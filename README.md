# Discord-Ship-by-ID-command
This program can take two Discord user IDs and calculate a value from 0% to 100%.

Example usage:
```python
from discord_shipping_1b import ship

print(ship(
  "LeeSpork", 431402543336390666,
  "Robot", 788531503138340914
))
```
```python
from discord_shipping_1b import snowflake_compatability as ship_value

user1 = 431402543336390666
user2 = 788531503138340914
value = ship_value(431402543336390666, 788531503138340914)

print(f"They are {value:.0%} compatible!")
```

The values at the top of the value `WEIGHT_00`, `WEIGHT_01`, and `WEIGHT_11` can be tweaked to change the distrubution of the output.
`debug_all_compatabilities()` is designed to test this, though you need a decent amount of sample data to do so.
`COMPATABILITY_BIT_MASK` can also be altered to change what bits are used or ignored in the algorithm. It is current set up to ignore most of the timestamp in the user IDs
to prevent the results from being reliant on account creation date.

`SHIP_THRESHOLD` is used by the `ship()` function to determine which message to output. The messages were written by RafaelScarpa for his Discord bot.
