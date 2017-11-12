# ionic-2-tabs-page-with-back-button
A simple wrapper-based solution for displaying a working back button in an "ionic 2" tabs page.
This is _one_ solution to ionic bug #5351 https://github.com/driftyco/ionic/issues/5351.

Note: since this project's creation, it has been upgraded to later versions of Ionic and Angular.
See the repo tags to view specific version upgrades.

The _tabs_ starter project was generated along with a landing page.
The root page of the app is set to the landing page. From within the landing page, a button
is provided to navigate to a wrapped tabs page, which is pushed onto the navigation stack.
The tabs page is a nested component inside of a boilerplate wrapper component. The wrapper
gets the navigation button and houses the tabs structure.

The tab pages themselves have their ion-header element deleted else a nested nav header would appear.
Instead, the tabs' parent that declares ion-tabs listens for the ion-select event emitted when
tabs are selected. That parent then double-dispatches to the wrapper by emitting a new event containing
the tab name. The wrapper then uses the tab name to dynamically update the nav bar title as you'd
normally see.

See:
* https://github.com/matoos32/ionic-2-tabs-page-with-back-button/blob/master/src/pages/tabs-wrapper/tabs-wrapper.html
* https://github.com/matoos32/ionic-2-tabs-page-with-back-button/blob/master/src/pages/tabs-wrapper/tabs-wrapper.ts
* https://github.com/matoos32/ionic-2-tabs-page-with-back-button/blob/master/src/pages/tabs/tabs.html
* https://github.com/matoos32/ionic-2-tabs-page-with-back-button/blob/master/src/pages/tabs/tabs.ts

## How to run this demo
After cloning the repo:
1. Navigate to the project folder.
2. _npm install_
3. _ionic serve_
4. In your launched browser window click on the tabs page button.

