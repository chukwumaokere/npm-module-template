# NPM Module Template

## How to use
Clone this repo (Don't fork. So the repo can exist independently of this one)  
Fill `src/lib/components` with your components and CSS  
Fill `src/lib/libs` with your APIs and hooks  
Fill `src/lib/views` with your rendered out views like the Moderation settings page or Overlay setting page.    
Fill `/.env` with any environment variables you might need  

In `src/lib/index.js` import what you want to have available, and export it like

`src/lib/index.js`
```js
import Overlay from './views/Overlay';
import Button from './components/Button';

export { Overlay };
export { Button };
```

So you can do this on any platform: 
```js
import { Overlay as RaidersOverlay } from '@stream-captain/raiders-tools';
import { Button } from '@stream-captain/raiders-tools';


<Button props={props} />
<RaidersOverlay props={props} />
```

Update version number in `package.json`   
Run `npm run build` To build the latest one   
Commit everything (including `dist`)   
Then run `npm publish` to publish   