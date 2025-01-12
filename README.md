# GDQ stats

The raw data collected by my various [gdq trackers](https://gdq.alligatr.co.uk).

## Format

Each file has this shape:

```
{
  "marathon_name": "name here",
  "marathon_type": "gdq",
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

`marathon_type` is `gdq` for AGDQ and SGDQ, `ff` for Frame Fatales, and `gdqx` for GDQx.

More properties were added over time:
- The donation count was added in AGDQ 14
- The runners were added in AGDQ 15
- The category was added in SGDQ 20
