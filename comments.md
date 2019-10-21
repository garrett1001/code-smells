# Comments

Code without comments or incorrect comments makes it harder to read and for others to understand how the code function.s

```{dart}

/*
 * Select Base
 */
class Cart extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Custom Shakes',
      theme: new ThemeData(primaryColor: Color.fromRGBO(74, 101, 114, 1.0)),
      home: Scaffold(
        body: Center(
            child: Carts()
        ),
      ),
    );
  }
}

class CartState extends State<Carts> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: _buildCart(),
    );
  }

```

```{JavaScript}
const HomeScreen = (props) => {
  return (
  <View>
    <Text style={styles.text}>Care Map</Text>
    <TouchableOpacity onPress={() => props.navigation.navigate("Components")}>
      <Text>Go To Components</Text>
    </TouchableOpacity>
  <TouchableOpacity onPress={() => props.navigation.navigate("List")}>
      <Text>Go to List</Text>
    </TouchableOpacity>
    <TouchableOpacity onPress={() => props.navigation.navigate("Rate Us")}>
      <Text>Go to Rating</Text>
    </TouchableOpacity>
  </View>
  );
};
```
