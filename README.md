Project for time series forecasting with machine learning. 

Cleaned dataset changes:
- zeros filled with previous prices for price dfs
- duplicate entries removed(all previous prices = current prices)

Features:
- Previous buy prices up to stepsBack
- Current buy quantity
- Current capital flow (cf = currentPrice * currentQuantity)

Layers:
- encoder(2 LSTM)
- decoder(2 LSTM)(teacher forcing)
- timeDistributed(Dense)

Loss:
- Huber
- mse
- custom for multiple outputs
