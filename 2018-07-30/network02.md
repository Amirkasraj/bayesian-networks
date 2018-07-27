- Look at the data at folder `data`.
- Each file is downloaded from website [http://tsetmc.ir/Loader.aspx?ParTree=151311&i=44891482026867833](http://tsetmc.ir/Loader.aspx?ParTree=151311&i=44891482026867833) and tab 'History (سابقه)'. Look at persian names to understand the structure of data.
- For now just consider the column `Close`. For each data file, convert `Close` column into a discrete time-series, e.g. with values in { 1, 0, -1 } or { decrease, nochange, increase }.
- Call them <img src="https://latex.codecogs.com/svg.latex?\left\lbrace&space;X^1_{t},&space;\cdots,&space;X^{20}_{t}&space;\right\rbrace" title="\left\lbrace X^1_{t}, \cdots, X^{20}_{t} \right\rbrace" />

Create an analogue of `network01.md` for this dataset as follows:
1. Choose one, for example <img src="https://latex.codecogs.com/svg.latex?X^1_{t}" title="X^1_{t}" />, to predict
2. For other 19 time-series, <img src="https://latex.codecogs.com/svg.latex?\left\lbrace&space;X^{2}_{t},&space;\cdots,&space;X^{20}_{t}&space;\right\rbrace" title="\left\lbrace X^{2}_{t}, \cdots, X^{20}_{t} \right\rbrace" />, add their lags (first three lags as in `network01`) as nodes and connect them to <img src="https://latex.codecogs.com/svg.latex?X^1_{t}" title="X^1_{t}" />
3. Example connections for <img src="https://latex.codecogs.com/svg.latex?X^2" title="X^2" />: <img src="https://latex.codecogs.com/svg.latex?X^{2}_{t-1}&space;\Rightarrow&space;X^1_{t}" title="X^{2}_{t-1} \Rightarrow X^1_{t}" />,
<img src="https://latex.codecogs.com/svg.latex?X^{2}_{t-2}&space;\Rightarrow&space;X^1_{t}" title="X^{2}_{t-2} \Rightarrow X^1_{t}" />,
<img src="https://latex.codecogs.com/svg.latex?X^{2}_{t-3}&space;\Rightarrow&space;X^1_{t}" title="X^{2}_{t-3} \Rightarrow X^1_{t}" />
4. Create and save the diagram
5. Analyze the network using __Samiam__.
    - If we know the information, what results can we predict accurately?
    - What we cannot predict accurately?
    - Which parameters are playing important role?
    - Can we check the behavior in time or we have only one final result? Can we observer different behaviors through time?
    - Can we add more indicators?
    - Can we use these networks to select important time-series?
    - Add more Q/A to the analysis