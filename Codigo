import 'package:flutter/material.dart';

void main() {
  runApp(const Myapp());
}

class Myapp extends StatelessWidget {
  const Myapp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: _Homepage(),
    );
  }
}

class _Homepage extends StatefulWidget {
  const _Homepage({Key? key}) : super(key: key);

  @override
  State<_Homepage> createState() => _HomepageState();
}

class _HomepageState extends State<_Homepage> {
  int count = 0;

  void decrement() {
    setState(() {
      count--;
    });

   print(count);
   }

   void increment() {
     setState(() {
       count++;
     });
   print(count);
   }
  bool get isEmpty => count== 0;
  bool get isFull  => count==20;

   @override
   Widget build(BuildContext context) {
   return Scaffold(
    backgroundColor: Colors.red,
      body: Container(
        decoration: const BoxDecoration(
        image: DecorationImage(
        image: AssetImage('assets/images/imagem.jpg'),
        fit: BoxFit.cover,
        ),
        ),
        child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
           Text(
            isEmpty? "Vazio":isFull ? "Lotado":'Pode entrar',
              style: TextStyle(
                fontSize: 30,
              color: isFull?Colors.red:Colors.black,
              fontWeight: FontWeight.w700,
              ),
          ),
          Padding(
             padding: EdgeInsets.all(40),

            child: Text(
              "$count",
                style:  TextStyle(
                 fontSize: 100,
                   color: isFull ? Colors.red: Colors.black,
                 ),
                 ),
                 ),
              Row(
                 mainAxisAlignment: MainAxisAlignment.center,
                 children: [
                   TextButton(
                     onPressed: isEmpty ? null: decrement,
                     style: TextButton.styleFrom(
                     backgroundColor: isEmpty ? Colors.white54: Colors.white,
                     fixedSize: const Size(100, 100),
                     primary: Colors.black,
                     shape: RoundedRectangleBorder(
                     borderRadius: BorderRadius.circular(24),
                     ),
                     ),
                      child: const  Text(
                        "saiu",
                       style:  TextStyle(
                       color: Colors.black,
                       fontSize: 16,
                       ),
                       )),

                const SizedBox(
                 width: 32
                 ),
                TextButton(onPressed: isFull ?null: increment,
                   style: TextButton.styleFrom(
                   backgroundColor: isFull ? Colors.white54:Colors.white,
                   fixedSize: const Size(100, 100),
                   primary: Colors.black,
                   shape: RoundedRectangleBorder(
                   borderRadius: BorderRadius.circular(24),
                   ),
                   ),
                  child:  Text(
                    "Entrou",
                     style:  TextStyle(
                     color: Colors.black,
                     fontSize:16,
                      ),
                    )
                ),
                 ],
              ),
            ],
        ),
      ),
   );
  }
}

