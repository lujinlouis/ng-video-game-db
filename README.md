# NgVideoGameDb

Application will send API requests to "https://rawg-video-games-database.p.rapidapi.com" to get game db data.

`getGameList` and `getGameDetails` functions in **Angular Service** file `http.service.ts` send API requests to get back **Observables** and we subscribe the **Observables** in component ts files to get the data.

Error interceptor inserts error state to the API requests. Header interceport inserts the header and key to the API requests.

`search-bar` component sends the `game-search` as **Route Params** to `home` component. Then `home` component sends the API request with data from `game-search` params using service `getGameList`. 

`home` component sends the game id as **Route Params** to `details` component. `details` component then sends the API request with data from game id params using service `getGameDetails`.

`details` component passes the `game` parameter to child component `game-tabs`. `game-tabs` component then dispay the tabs based on the data in `game` parameter

`mwl-gauge` from module **angular-gauge** to provide the "gauge" view in game details page.

`mat-tab-group` from **Angular Material tabs** to provide "tabas" view in game details page.




