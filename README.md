WaveTrend Pyramiding Strategy

This script implements a complete trading strategy based on the WaveTrend oscillator (LazyBear model), combined with automatic pyramiding, trend-reversal exits, and a full state-tracking system for multi-layered positions.

Key Features:

WaveTrend calculation (WT1 & WT2) using ESA, deviation, CI, and TCI formulas.
Long/Short entries triggered only when price reaches overbought/oversold zones and WT1 crosses WT2.
Automatic pyramiding:
Adds Long layers only when price is below the previous entry.
Adds Short layers only when price is above the previous entry.

Reversal logic:

Long → Short when WT1 confirmed overbought and crosses under WT2.
Short → Long when WT1 confirmed oversold and crosses over WT2.

State tracking for:

Current mode (neutral / long / short)
Last entry price
Number of layers added
Overbought/oversold confirmations

How the Strategy Works:

Long Entry: WT1 is below -40 and crosses above WT2.
Short Entry: WT1 is above +40 and crosses under WT2.
Pyramiding: Adds positions only if the new price improves the average entry.
Exit + Reverse: When WT1 confirms an extreme + a WT1/WT2 cross in the opposite direction.
All trades are managed through TradingView’s strategy.entry() and strategy.close() functions.

Purpose:

This strategy is designed for users who want a structured, rule-based system that captures extended market moves using WaveTrend momentum.
It avoids noise signals, respects trend structure, and allows deeper position building under controlled conditions.

Ideal For:

Backtesting trend systems
Learning WaveTrend behavior
Building custom WT-based strategies
Exploring pyramiding logic in TradingView
