# React Navigation
(notes from reactnavigation.org and tangential topics)

* `npm install --save react-navigation`

* definitely revisit the differences between `react-native init` and
`create-react-native-app`



### Stack Navigator
* `import { StackNavigator } from 'react-navigation'`

#### Screen Navigation Options
* screens can configure several aspects about how they are presented in
parent navigators

**Static Configuration**
* each navigation option is directly assigned:
  * `static navigationOptions = { title: 'Great' };`

**Dynamic Configuration**
* options an be a function that returns an object navigationOptions that
will override previously defined navigationOptions


# Navigators
* define your app's navigation structure
* render elements like headers and tab bars
* (they're just plain react components)

##### Built-in Navigators
* StackNavigator
* TabNavigator
* DrawerNavigator

##### Use above to render new application screens (react components)
* `navigation` prop allows screen to dispatch navigation actions
* `navigationOptions` customizes how the screen gets presented

##### Navigating from the Top Level components
* if using a navigator from the same level you declare it, use `ref`

##### Navigation Containers
* built-ins can behave like top-levels when `navigation` prop is missing
* the prop will come from a transparent container courtesy of `createNavigationContainer`, which is used behind the scenes
* navigators usually require the `navigation` prop to function
* the container can also handle URLs, external linking, back buttons

**Top-level navigator props:**
* `onNavigationStateChange(prevState, newState, action)` is called every
time the navigation state managed by the navigator changes
  * prints state changes to console
* `uriPrefix` for handling a deep link to extract the path passed to the
router

*******

# StackNavigator
* transition between screens when a new one is placed at the top of the
stack


***********

# Linking

* API that gives general interface to interact with incoming/outgoing app links
