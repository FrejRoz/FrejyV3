# FrejyV3
BB Entry with POC Filter - Hybrid Strategy Indicator
This indicator is a high-precision trading tool that combines mean-reversion Bollinger Bands (BB) logic with a volume-based Point of Control (POC) filter. It is designed to filter out "counter-trend" noise by ensuring that signals only fire when price action aligns with the heaviest traded volume zone.

🚀 Key Features
DIY Volume Profile (POC): Calculates the Point of Control (the price level with the highest volume) over a custom lookback period without requiring a premium TradingView plan.

Directional Bias Filter: Automatically switches signal logic based on price location relative to the POC. (Price > POC = Longs Only | Price < POC = Shorts Only).

Time-Locked Execution: Includes a precise start-time filter to begin trading only after specific market events or sessions.

Live Average Entry Tracker: Calculates and displays your average entry price in real-time for scaling-in strategies.

📈 Trading Logic & Entry Criteria
The indicator validates signals through a two-step confirmation process:

1. The Directional Filter (POC)
The yellow line represents the high-volume anchor.

Long Bias: The strategy only looks for Buy signals when the current price is above the POC line.

Short Bias: The strategy only looks for Sell signals when the current price is below the POC line.

2. Bollinger Band Triggers
Users can choose between two distinct entry modes depending on their risk appetite:

Bottom Only (Sniper Mode):

Long: Fires only when the low touches the lower BB band while price is above POC.

Short: Fires only when the high touches the upper BB band while price is below POC.

Ideal for capturing exact reversals at the extremes.

Bottom to Center (Continuous Entry):

Once a band is touched, a "buying/selling state" becomes active. The indicator will continue to signal entries as long as the price remains between the outer band and the middle basis line.

Ideal for scaling into a position or trend-following momentum.

⚙️ Configuration (Inputs)
Time Filter
Use Start Date Filter: Enable/Disable the start time restriction.

Start Date/Time: Set the exact Year, Month, Day, and Minute to begin signal generation.

Strategy Settings
Trade Side: Choose between "Long", "Short", or "Both".

Entry Mode: Switch between "Bottom Only" (one-time touch) and "Bottom to Center" (state-based entries).

BB Length & StdDev: Standard Bollinger Band parameters (Default is 20/2.0).

POC Filter Settings
POC Lookback Bars: The window of bars used to calculate the volume profile.

POC Price Rows: The vertical resolution of the volume profile (Higher = More precise POC).

📊 Visual Interface
Yellow Line: The calculated Point of Control.

Green/Red Labels ($): Visual entry signals on the chart.

Dashboard (Table): A floating table on the right showing the Average Entry Price for the current active trade cycle.
