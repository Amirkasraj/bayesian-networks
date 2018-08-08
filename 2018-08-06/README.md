# `2018-08-06`
Do the following tasks in addition to tasks in [Trello#1397-05-15](https://trello.com/c/87ECsXGu).

1. Modify the file `bayesian_networks.py` so that it contains two classes
    - `bayesian_networks.Full`: makes a complete graph given name of parameters and number of delays, e.g. _a complete graph with `parameters=['Gold','EUR'], lag=1` has `4` nodes and `6` edges._

    <img width="200" alt="Full Graph" src="https://raw.githubusercontent.com/Amirkasraj/bayesian-networks/master/2018-08-06/full_graph.png">

    - `bayesian_networks.Cascade`: makes a complete graph without the target's future and then connect all to it, e.g. _a cascade graph with `target=['Gold'], parameters = ['EUR'], lag = 2` has `5` nodes and `10` edges._

    <img width="200" alt="Cascade Graph" src="https://raw.githubusercontent.com/Amirkasraj/bayesian-networks/master/2018-08-06/cascade.png">

    - `bayesian_networks.RangedGrid` makes something like a grid but more symmetric and more sophisticated, e.g. _a grid graph with `parameters = ['Gold','EUR'], lag = 3, depth = 2` will have `8` nodes and `24` edges_.

    <img width="200" alt="Full Graph" src="https://raw.githubusercontent.com/Amirkasraj/bayesian-networks/master/2018-08-06/grid_depthed.png">

2. Each class should (at leas) contain the following methods:
    - `train(data)` which trains the weights of the network with given `data` formatted as:
    ```
    Gold,EUR,JPY
    increased,increased,decreased
    decreased,increased,unchanged
    ...
    ```
    _for now, assume that the data is complete and there is no missing information._
    - `query(targets, conditions)` which computes the probabilities of `targets` conditioned on given `conditions`. Example
    ```
    targets = [ 'Gold', 'EUR', ... ]
    conditions = { 'JPY': 'increased', 'GBP': 'decreased', ... }
    ```
    - `visualize()` which draws some visualization of the graph of network.
















