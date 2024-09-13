<h1>DropDownSearchField</h1>

<p><strong>DropDownSearchField</strong> is a customizable Flutter widget that provides a searchable dropdown menu. This widget allows users to filter and select items from a list in real-time, making it ideal for forms and search-driven applications.</p>

<h2>Features</h2>
<ul>
  <li>Real-time search and filtering functionality.</li>
  <li>Customizable dropdown UI with support for item builders.</li>
  <li>Error widget for handling empty search results.</li>
  <li>Configurable dropdown menu height, background color, and decoration.</li>
  <li>Custom input decoration and validation support.</li>
</ul>

<h2>Installation</h2>

<p>Add the following dependency in your <code>pubspec.yaml</code> file:</p>

<pre><code>dependencies:
  dropdown_search_field: ^0.0.1
</code></pre>

<p>Then, run <code>flutter pub get</code> to install the package.</p>

<h2>Usage</h2>

<p>Here’s a basic example of how to use the <strong>DropDownSearchField</strong> widget:</p>

<pre><code>import 'package:flutter/material.dart';
import 'package:dropdown_search_field/dropdown_search_field.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: Text('DropDownSearchField Example')),
        body: Padding(
          padding: const EdgeInsets.all(16.0),
          child: DropDownSearchField(
            items: ['Apple', 'Banana', 'Orange', 'Pineapple'],
            controller: TextEditingController(),
            itemBuilder: (context, item) {
              return ListTile(title: Text(item));
            },
            onSelected: (value) {
              print('Selected: $value');
            },
          ),
        ),
      ),
    );
  }
}
</code></pre>

<h2>Parameters</h2>

<ul>
  <li><strong>items</strong>: List of items to be displayed in the dropdown.</li>
  <li><strong>controller</strong>: TextEditingController to manage the input field.</li>
  <li><strong>itemBuilder</strong>: A function to build each dropdown item.</li>
  <li><strong>onSelected</strong>: Callback function when an item is selected.</li>
  <li><strong>textFormFieldDecoration</strong>: Custom decoration for the input field.</li>
  <li><strong>textFormFieldvalidator</strong>: Custom validator for the input field.</li>
  <li><strong>menuHeight</strong>: Maximum height for the dropdown menu.</li>
  <li><strong>menuBgColor</strong>: Background color for the dropdown menu.</li>
  <li><strong>errorWidget</strong>: Widget to display when no items match the search.</li>
  <li><strong>onChanged</strong>: Callback function triggered on text change.</li>
  <li><strong>onTap</strong>: Callback for input field tap event.</li>
</ul>

<h2>Contributing</h2>

<p>Contributions are welcome! Feel free to open an issue or submit a pull request.</p>

<h2>License</h2>

<p>This project is licensed under the MIT License.</p>
