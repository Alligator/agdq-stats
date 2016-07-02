# agdq stats
I decided that these stats should live somewhere more permanent than /var/www on my server.

## formats
The format changed over the years, here is a description of each:

### SGDQ13

The script ran every five minutes, but there are some gaps in the viewer counts as the script broke a few times. No donation totals as of yet, just viewers.

    {
      "games": [
        [start_timestamp, game_name],
        ...
      ],
      "viewers": [
        [timestamp, viewer_count],
        ...
      ]
    }

### AGDQ14

Donation count added, interval changed to one minute. I don't *think* the script has handling failures gracefully yet so there might be gaps in the viewers list (i.e there's not a record for every minute).

    {
      "games": [
        [start_timestamp, game_name],
        ...
      ],
      "viewers": [
        [timestamp, viewer_count, dontation_total],
        ...
      ]
    }

### SGDQ14

Same as AGDQ14, but now more resilient, so there should be nulls where the script couldn't get data and a record for every minute it was running.

### AGDQ15

Same as SGDQ14 but with the runner(s) name. As an aside, this file is called agdq15-scraped because the donation totals were scraped from the tracker after the marathon ended as my original stats file had a lot of gaps and was entirely missing the final push.

    {
      "games": [
        [start_timestamp, game_name, runner_name],
        ...
      ],
      "viewers": [
        [timestamp, viewer_count, dontation_total],
        ...
      ]
    }

*Everything after AGDQ15 uses the same format.*
