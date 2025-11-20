WaveTrend Pyramiding Strategy – Description

This script implements a full WaveTrend-based trading strategy with automatic pyramiding, trend-reversal exits, and position-switching logic.
It is designed for users who want a structured, rules-based system built around the classic LazyBear WaveTrend oscillator.

Core Features

WaveTrend (WT1 & WT2) calculation using the standard ESA/CI/TCI model.

Dynamic Long/Short detection based on overbought/oversold zones (+40 / -40) combined with WT1–WT2 crossovers.

Automatic pyramiding:

Adds to Long positions only below the previous entry price.

Adds to Short positions only above the previous entry price.

Full position reversal logic:

If a Long hits overbought and WT1 crosses below WT2 → reverse into Short.

If a Short hits oversold and WT1 crosses above WT2 → reverse into Long.

State tracking system to keep control during multi-entry pyramiding:

Mode (Long / Short / Neutral)

Entry price per layer

Number of accumulated entries

Overbought/Oversold confirmation flags

How It Works

Enters Long when WT1 is below -40 and crosses above WT2.

Enters Short when WT1 is above +40 and crosses under WT2.

Adds to the position only if the new price improves the average entry.

Closes & reverses only after WT1 has confirmed an extreme (OB/OS) and a trend cross occurs.

Uses built-in TradingView strategy.entry() and strategy.close() to manage full pyramiding up to 50 layers.

Why This Strategy

It avoids random scalping signals and waits for WT structure confirmation, not just a single crossover.
By combining:

momentum confirmation

directional crossovers

controlled pyramiding

… the strategy focuses on capturing extended trend waves, not small noise moves.

Intended Use

Backtesting trend-based systems

Studying WaveTrend structure

Experimenting with pyramiding logic

Creating custom WT-based automated strategies
