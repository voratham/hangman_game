## Hangman game core with elixir lang


### How to run
```sh
cd hangman
mix test // run unit-test
iex -S mix

iex(1)> game = Hangman.new_game
%Hangman.Game{
  turns_left: 7,
  game_state: :initializing,
  letters: ["j", "a", "v", "a", "s", "c", "r", "i", "p", "t"],
  used: MapSet.new([])
}
iex(2)> { game ,tally } = Hangman.make_move(game, "j")
{%Hangman.Game{
   turns_left: 7,
   game_state: :good_guess,
   letters: ["j", "a", "v", "a", "s", "c", "r", "i", "p", "t"],
   used: MapSet.new(["j"])
 },
 %{
   game_state: :good_guess,
   letters: ["j", "_", "_", "_", "_", "_", "_", "_", "_", "_"],
   turns_left: 7
 }}
iex(3)> tally
%{
  game_state: :good_guess,
  letters: ["j", "_", "_", "_", "_", "_", "_", "_", "_", "_"],
  turns_left: 7
}
```