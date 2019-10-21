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