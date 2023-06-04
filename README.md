# GDQ stats

The raw data collected by my various [gdq trackers](https://gdq.alligatr.co.uk).

## Format

Each file has this shape:

```
{
  "games": [
    [start_timestamp, game_name, runners, category],
    ...
  ],
  "viewers": [
    [timestamp, viewer_count, donation_count],
    ...
  ]
}
```

More properties were added over time:
- The donation count was added in AGDQ 14
- The runners were added in AGDQ 15
- The category was added in SGDQ 20
