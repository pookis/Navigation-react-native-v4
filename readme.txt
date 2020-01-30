npm install react-navigation-drawer

import { createDrawerNavigator } from 'react-navigation-drawer';

createDrawerNavigator(RouteConfigs, DrawerNavigatorConfig);

https://reactnavigation.org/docs/en/drawer-navigator.html
--------

npm install react-navigation-stack @react-native-community/masked-view

import { createStackNavigator } from 'react-navigation-stack';

createStackNavigator(RouteConfigs, StackNavigatorConfig);

createStackNavigator({
  // For each screen that you can navigate to, create a new entry like this:
  Profile: {
    // `ProfileScreen` is a React component that will be the main content of the screen.
    screen: ProfileScreen,
    // When `ProfileScreen` is loaded by the StackNavigator, it will be given a `navigation` prop.

    // Optional: When deep linking or using react-navigation in a web app, this path is used:
    path: 'people/:name',
    // The action and route params are extracted from the path.

    // Optional: Override the `navigationOptions` for the screen
    navigationOptions: ({ navigation }) => ({
      title: `${navigation.state.params.name}'s Profile'`,
    }),
  },

  ...MyOtherRoutes,
});


https://reactnavigation.org/docs/en/stack-navigator.html

-----------

npm install react-navigation-tabs

import { createBottomTabNavigator } from 'react-navigation-tabs';

createBottomTabNavigator(RouteConfigs, TabNavigatorConfig);

https://reactnavigation.org/docs/en/bottom-tab-navigator.html

-------------
import { createAppContainer } from 'react-navigation';
------------------
npm install --save react-native-vector-icons
-------------
npm install --save @react-native-community/masked-view
-------------
npm install react-native-safe-area-context

-----------

Deprecation in 'navigationOptions':
- 'headerTitle: <SomeElement />' will be removed in a future version. Use 'headerTitle: () => <SomeElement />' instead
- 'headerLeft: <SomeElement />' will be removed in a future version. Use 'headerLeft: () => <SomeElement />' instead
