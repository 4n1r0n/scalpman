# Opposing Tick Zones

Version 0.1.1.

A Pine Script v6 chart indicator based on TradingLab’s short [How To Find PERFECT Entries](https://www.youtube.com/shorts/tS9o8aQjADY).

On a 1 hour trend, mark the highest tick of the lowest bar and the lowest tick of the highest bar. Those two bars are the demand and supply areas. Trade the area price hits first, after it holds and price comes back to the tick.

## Rules

1. Find the highest bar and the lowest bar of the trend. Swing strength (default 3) is how the script picks them. The short marks them by eye.
2. Demand is the lowest bar. The tick is its high. The area runs down to that bar’s low.
3. Supply is the highest bar. The tick is its low. The area runs up to that bar’s high.
4. After price is sitting between them, the first area it hits is the only side. Demand first means longs. Supply first means shorts.
5. Enter when that area holds and price comes back to the tick.
6. Long stop is below demand, target is the high. Short stop is above supply, target is the low.
7. A print beyond either extreme cancels the idea. That bar becomes the new high or low.

## Add it in TradingView

1. Open a chart. The short uses the 1 hour chart.
2. Open the Pine Editor.
3. Paste `opposing-tick-zones.pine`.
4. Click Add to chart.

Version 0.1.1 fixes TradingView runtime error 10026. The zones are drawn from the pivot bar’s time, so a long chart no longer rejects the old bar index. The rules are unchanged from 0.1.
