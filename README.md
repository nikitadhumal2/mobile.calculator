// This is a basic example and needs to be expanded
import React, { useState } from 'react';
import { View, Text, TouchableOpacity, StyleSheet } from 'react-native';

const App = () => {
  const [displayValue, setDisplayValue] = useState('');
  const handlePress = (value) => {
    setDisplayValue(displayValue + value);
  }

  return (
    <View style={styles.container}>
        <View style={styles.displayContainer}>
          <Text style={styles.displayText}>{displayValue}</Text>
        </View>
        <View style={styles.buttonContainer}>
          <TouchableOpacity style={styles.button} onPress={()=> handlePress('1')}>
            <Text>1</Text>
          </TouchableOpacity>
          {/* add more buttons */}
        </View>
    </View>
  );
};

const styles = StyleSheet.create({
    container: {
        flex: 1,
        padding: 20,
    },
    displayContainer:{
      flex:1,
      justifyContent:'flex-end',
    },
    displayText: {
        fontSize: 48,
    },
    buttonContainer: {
        flex: 2,
        flexDirection: 'row',
    },
    button: {
      backgroundColor: '#dddddd',
      flex:1,
      justifyContent: 'center',
      alignItems: 'center',
    }
});

export default App;
