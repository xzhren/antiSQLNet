# antiSQLNet
SQL Injection Detection Network

## Files Introduction

- 001#DataProprocess
  - Put Json Data to CSV: train.csv(3w), test.csv(20w), test2.csv(20w)
  - train.csv: id, label, value
  - test.csv: id, value
  - test2.csv: (error: id, label, value)

- 002#DataVisual
  - get vocab & label value, vocab size 70
  - max of len is 11553, get len < 1000
  - sample negative 2500*2
  - Bi-LSTM Faild

- 003#DynamicRNN
  - get vocab & label value, vocab size 70
  - 75% of len is 100, get len < 500
  - Counter({0: 27159, 1: 1973})
  - sample negative 4000
  - padding & batcher
  - Bi-LSTM 95.375

- 004#DLSTM-TensorBoard
  - label vocab & label encoder & balanced sampele & padding & one-hot
  - Batcher 80% tain
  - Bi-LSTM & tensorboard 95.525
  - test accuracy & diff output

- 005#bi-GRU
  - label vocab & label encoder & balanced sampele & padding & one-hot
  - Batcher 80% tain
  - Bi-GRU & tensorboard 95.625
  - test accuracy & diff output

- 999#TestDynamicRNN
- 999#TestIMDB