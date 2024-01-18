# CityLearn

CityLearn is an open source OpenAI Gym environment for the implementation of Multi-Agent Reinforcement Learning (RL) for building energy coordination and demand response in cities. A major challenge for RL in demand response is the ability to compare algorithm performance. Thus, CityLearn facilitates and standardizes the evaluation of RL agents such that different algorithms can be easily compared with each other.

![Demand-response](https://github.com/intelligent-environments-lab/CityLearn/blob/master/assets/images/dr.jpg)

## Environment Overview

CityLearn includes energy models of buildings and distributed energy resources (DER) including air-to-water heat pumps, electric heaters and batteries. A collection of building energy models makes up a virtual district (a.k.a neighborhood or community). In each building, space cooling, space heating and domestic hot water end-use loads may be independently satisfied through air-to-water heat pumps. Alternatively, space heating and domestic hot water loads can be satisfied through electric heaters.

![Citylearn](https://github.com/intelligent-environments-lab/CityLearn/blob/master/assets/images/citylearn_systems.png)

## Installation

Install latest release in PyPi with `pip`:

```console
pip install CityLearn
```

## Documentation

Refer to the [docs](https://intelligent-environments-lab.github.io/CityLearn/) for documentation of the CityLearn API.

## Trading Environment Progress

The aim of this forked package is to allow power trading behavior for Buildings class.
This is composed of multiple steps ordered in increasing order of difficulty :

- Understand CityLearn package
- ✅ Allow Building class the action to trade with the grid (buy and sell power stored in Battery class)
- ✅ Update Battery electricity storage when trading power
- ✅ Allow CityLearn Environment to evaluate new trading behavior
- ✅ Define new KPIs including new behavior (trade earning)
- ✅ Derive new Reward function to make decisions sensible to power trade earnings
- ✅ Train RL model (SAC & Q-Learning) on new trade actions and observe improvements
- ❌ Transform Environment in order to share information about Buildings will to buy/sell power between each other
- ❌ Build Price Agreement rules to exchange power between 2 (or more) Buildings
- ❌ Train RL model with building able to trade between each other
