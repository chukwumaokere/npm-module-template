# NPM Module Template

## How to use
1. Clone this repo (Don't fork. So the repo can exist independently of this one)  
2. Change all references of `npm-module-template` to `your-product-name`  
3. Run `npm install` to install all the dependencies as needed
4. Fill `src/lib/components` with your components and CSS  
5. Fill `src/lib/libs` with your APIs and hooks  
6. Fill `src/lib/views` with your rendered out views like the Moderation settings page or Overlay setting page.    
7. Fill `/.env` with any environment variables you might need  
8. You can use /App.js to render out your components and see what they'll look like as you build them.  

In `src/lib/index.js` import what you want to have available, and export it like this:
### Exporting
`src/lib/index.js` should look like this:
```js
import Overlay from './views/Overlay';
import Button from './components/Button';

export { Overlay };
export { Button };
```

### Consuming
So you can do this on any React platform: 
```js
import { Overlay as RaidersOverlay } from '@stream-captain/your-product-name'; //your product name can be like @stream-captain/raiders-tools
import { Button } from '@stream-captain/your-product-name';


<Button props={props} />
<RaidersOverlay props={props} />
```
### Publishing 
1. Update version number in `package.json`   
2. Run `npm run build` To build the latest one   
Commit everything (including `dist`)
Make sure you're logged in using `npm login` and your github personal access token (with read and write permissions as per [This guide](https://streamcaptain.atlassian.net/wiki/spaces/CT/pages/1734475809/Node+Modules)) as your password    
Then run `npm publish` to publish   