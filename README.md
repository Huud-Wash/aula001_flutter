import 'package:flutter/material.dart';

const Color darkBlue = Color.fromARGB(255, 18, 32, 47);

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData.dark().copyWith(
        scaffoldBackgroundColor: darkBlue,
      ),
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Center(
          child: MyWidget(),
        ),
      ),
    );
  }
}

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Column(children: [
      const Text('Cadastro NewUser'),
      const Padding(
        padding: EdgeInsets.all(10.0),
        child: TextField(
          decoration: InputDecoration(
            border: OutlineInputBorder(),
            labelText: 'Nome',
          ),
        ),
      ),
      const Padding(
        padding: EdgeInsets.all(10.0),
        child: TextField(
          decoration: InputDecoration(
            border: OutlineInputBorder(),
            labelText: 'Endereço',
          ),
        ),
      ),
      const Padding(
        padding: EdgeInsets.all(10.0),
        child: TextField(
          decoration: InputDecoration(
            border: OutlineInputBorder(),
            labelText: 'Telefone',
          ),
        ),
      ),
      Image.network(
        'https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/cc37b6ed-4124-463b-9e1b-64e8f09b59cc/dcf1md2-5827d075-7c56-40c0-870a-e3106a6ab8dc.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcL2NjMzdiNmVkLTQxMjQtNDYzYi05ZTFiLTY0ZThmMDliNTljY1wvZGNmMW1kMi01ODI3ZDA3NS03YzU2LTQwYzAtODcwYS1lMzEwNmE2YWI4ZGMucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.60vEkL1Br5vPvp_eldtdFCbD1_0OlQ_WiEMPa2wxkHs',
         height: 400,
      )
    ]);
  }
}
