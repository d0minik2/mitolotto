<h1 align="center">lotterySIM</h1>
<p align="center">
Lottery Simulations in Python <br> <br>
    <a href="#installation"> Installation  </a> | <a href="#usage">  Usage </a>
</p> 
<br>

<h2 align="center">Installation</h2>

```console
# clone the repository
TODO
```
#### or
```console
# install by pip directly from github
TODO
```

<br>

<h2 align="center">Usage</h2>


<h3 align="center">Usage with existing lotteries</h3>
Supported example lotteries: <a href="https://www.lotto.pl/lotto"> Lotto </a>, <a href="https://www.lotto.pl/eurojackpot"> EuroJackpot </a>
<br><br>

- Initialize simulation
```python
import lotterySIM

player = lotterySIM.Player()

lottery = lotterySIM.example_lotteries.Lotto()

simulation = lotterySIM.Simulation(
    lottery, player, rounds_per_week=3
    )
```
<br>

- Generate random guess
```python
player.generate_guess(lottery)
```
- **OR** set custom guess
```python
player.set_guess([23, 13, 12, 41, 34, 32], lottery=lottery)
```
<br>

- Simulate lottery until won the top price
```python
simulation.simulate_years_until_won(log=True)
```
```console
simulated 1205 years
money spent: 2349750.0
money won: 1742824
total balance: -606926.0
won the top price 0 times
...
```
<br>


<h3 align="center">Usage with custom lotteries</h3>
