# Goban JS
Simple Go board implementation in pure JavaScript
mainly used to serve as a GUI to query KataGo network
directly in a web browser

# Example usage
<a href="https://maksimkorzh.github.io/gobanjs/simple_goban.html">simple goban</a><br>
<a href="https://maksimkorzh.github.io/gobanjs/load_sgf.html">SGF viewer</a><br>
<a href="https://maksimkorzh.github.io/kata-model-js/">Play against pure KataGo neural network</a>

# API
```js
// Board class
const Goban = function(params) {
  ...
  return {
    init: init(),
    BLACK: BLACK,
    WHITE: WHITE,
    importSgf: function(sgf) { return loadSgf(sgf); },
    exportSgf: function() { return saveSgf(); },
    position: function() { return board; },
    setKomi: function(komiVal) { komi = komiVal; },
    komi: function() { return komi; },
    history: function() { return history; },
    side: function() { return side; },
    ko: function() { return ko; },
    count: function(sq, color) { return count(sq, color); },
    liberties: function() { return liberties; },
    restore: function() { return restoreBoard(); },
    play: function(sq, color, user) { return setStone(sq, color, user); },
    handicap: function(stones) { return setHandicap(stones); },
    pass: function() { return pass(); },
    refresh: function() { return drawBoard(); },
    undoMove: function() { return undoMove(); },
    firstMove: function() { return firstMove(); },
    prevFewMoves: function(few) { return prevFewMoves(few); },
    prevMove: function() { return prevMove(); },
    nextMove: function() { return nextMove(); },
    nextFewMoves: function(few) { return nextFewMoves(few); },
    lastMove: function() { return lastMove(); }
  }
}

// Create board
const goban = new Goban({
  'size': 19,
  'width': 800,
});
```
