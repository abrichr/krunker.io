<div align="center">
	<br>
  	<p>
		<a href="https://krunker.io"><img src="https://i.imgur.com/qvTc8OA.png" width="546"></a>
  	</p>
  	<br>
  	<p>
		<a href="https://www.npmjs.com/package/@fasetto/krunker.io">
			<img src="https://img.shields.io/npm/v/@fasetto/krunker.io.svg?maxAge=3600" alt="NPM version">
		</a>
		<a href="https://www.npmjs.com/package/@fasetto/krunker.io">
			<img src="https://img.shields.io/npm/dt/@fasetto/krunker.io.svg?maxAge=3600" alt="NPM downloads">
		</a>
		<a href="https://david-dm.org/fasetto/krunker.io">
			<img src="https://img.shields.io/david/fasetto/krunker.io.svg?maxAge=3600" alt="Dependencies">
		</a>
	</p>
  	<p>
		<a href="https://nodei.co/npm/@fasetto/krunker.io/">
			<img src="https://nodei.co/npm/@fasetto/krunker.io.png?downloads=true&stars=true" alt="npm installnfo">
		</a>
  	</p>
</div>

UnOfficial Api for interacting with the [Krunker.io Social Page](https://krunker.io/social.html)

## Setup and Installation

```
$ npm i @fasetto/krunker.io
```

## Getting Started

### Profile Informations
```js
const { Krunker: Api, OrderBy } = require("@fasetto/krunker.io")

const Krunker = new Api();

const PrintUserData = async () =>
{
    try
    {
        const user = await Krunker.GetProfile("fasetto");
        console.log(user);
    }
    catch (e)
    {
        // console.log(e.message);
        console.log("Sorry ):\nWe couldn't find that user!");
    }

}

// {
//   name:'fasetto',
//   id:124403,
//   score:842665,
//   level:27,
//   kills:7905,
//   deaths:5759,
//   kdr:'1.37',
//   spk:'106.60',
//   totalGamesPlayed:997,
//   wins:410,
//   loses:587,
//   wl:'0.41',
//   playTime:'3d 9h 33m',
//   funds:113,
//   clan:'PUSU',
//   featured:'No',
//   hacker:'Negative'
// }

PrintUserData();
```

### Leaderboard Informations
```js
const { Krunker: Api, OrderBy } = require("@fasetto/krunker.io")

const PrintLeaderboard = async () =>
{
    try
    {
        const leaderboard = await Krunker.GetLeaderboard(OrderBy.Funds)
        console.log(leaderboard);

    }
    catch (e)
    {
        console.log(e.message);
    }
}

PrintLeaderboard();
```

### Game Informations
```js
const { Krunker: Api, OrderBy } = require("@fasetto/krunker.io")

const PrintGameInfo = async () =>
{
    try
    {
        const gameInfo = await Krunker.GetGameInfo("FRA:piucd");
        console.log(gameInfo);

    }
    catch (e)
    {
        console.log(e.message);
    }
}

// {
//   region:'Frankfurt',
//   players:'8/8',
//   map:'ctf_Sandstorm',
//   custom:false
// }

PrintGameInfo();
```


## Contact

Discord: fasetto#5885
