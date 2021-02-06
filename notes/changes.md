# Changes

Parameterize `PieceValues`:

- Formerly `constexpr Value PieceValue[PHASE_NB][PIECE_NB] = {
  ` in `types.head`
    
- Now defined in `material.cpp` without contstant: `Value PieceValue[PHASE_NB][PIECE_NB] = {
`

- Referenced `extern` elsewhere so
we get only one copy.
  
- Mutated in `ucioption.cpp` using `PieceNames` table for options

