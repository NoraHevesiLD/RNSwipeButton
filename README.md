## React Native Swipe Button component

![](https://udaysravank.github.io/RNSwipeButton/rn-swipe-button.gif)

<img src="https://udaysravank.github.io/RNSwipeButton/rn-swipe-button.gif" width="400" />

<br>
Code for below screenshot
<br>

```
import React, {Fragment} from 'react';
import {Text, ToastAndroid} from 'react-native';
import thumbIcon from './assets/thumbIcon.png';

import SwipeButton from 'rn-swipe-button';

const App = () => {
  return (
    <View style={{padding: 15}}>
      <Text style={{color: '#700D99', fontSize: 25}}>
        React Native Swipe Button
      </Text>
      <Text style={{color: '#059478', fontSize: 30}}>**************</Text>
      <Text style={{color: '#140866', fontSize: 20}}>
        Set onSwipeSuccess callback and width
      </Text>
      <SwipeButton
        disabled={false}
        onSwipeSuccess={() => {
          ToastAndroid.showWithGravity(
            'Submitted successfully!',
            ToastAndroid.SHORT,
            ToastAndroid.CENTER,
          );
        }}
        width={200}
      />
      <Text style={{color: '#140866', fontSize: 20}}>
        Enabled and thumb icon
      </Text>
      <SwipeButton thumbIconImageSource={thumbIcon} />
      <Text style={{color: '#140866', fontSize: 20}}>Disabled</Text>
      <SwipeButton disabled={true} />
      <Text style={{color: '#140866', fontSize: 20}}>Set height</Text>
      <SwipeButton height={25} />
      <Text style={{color: '#140866', fontSize: 20}}>Set height and width</Text>
      <SwipeButton height={35} width={150} title="Swipe" />
    </View>
  );
};
```

<br>
The below screenshot is from demo app under examples folder in the repo
<hr>
<img src="https://udaysravank.github.io/RNSwipeButton/rn-swipe-button.png" width="400" />

