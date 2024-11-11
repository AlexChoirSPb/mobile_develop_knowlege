Перетаскивание можно реализовать с помощью  двух основных виджетов: DragTarget и Draggable:
```dart
class MyApp extends StatelessWidget {
	@override
	Widget build(BuildContext context) {
	return MaterialApp(home: Scaffold(
		body: Center(child: Column(mainAxisAligment: MainAxisAligment.center,
			children: [
				DragTarget: (
					builder: (
						BuildContext context,
						List<String> accepted,
						List<String> rejected) {
							return new Container(
								width: 200, height: 200, color: Colors.lightBlue,
							);
						},
					onAccept: (data) => print(data),
				)
				Container(height: 50),
				Draggable(
					data: "I was dragged",
					child: Container(width: 100, height: 100, color: Colors.red),
					feedback: Container(width: 100, height: 100, color: Colors.yellow),
				)
			]
		))
	))}

}
```
DragTarget указывает на то, куда можно перетаскивать объект, 