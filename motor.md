#Unsere Motorsteuerung

damit der calliope fahren brauch er zum einen die hardware und andererseitz 
die Programirung...[die hardware ist hier zu finden](https://github.com/Mcccake/calliope-car/blob/master/Hardware.md)

##
Als erstes müssen wir den editor [makecode](https://makecode.calliope.cc) aufruen 

 (imgfahren)
 
 Als erstes  müssen wir eine Verbindung zwischen den beiden Calliope herstellen also nehmen wir die 
  baustene setze übertragung und setzte funkstäreke von dem Kasten Funk und packen 
  es in die Startschleife, das machen wir in beide Calliope projekte (Vernsteuerung und Motor)

Damit unser Auto später einmal Autonom fahren kann machen wir eine funktion die wir 
AmpelSystem nänen.  Mit dieser Funktion wollen wir erreichn das das auto nie gegen ein hindernis fährt 
da es ja keinen Rückwertsgang hat (kann man auch nicht Programmieren). 
In unsere Funktion packen wir ein Logik Element nämlich das wenn dann sonst wenn dann,ansonsten...
Als erstes wollen wir kucken ob ein element vor unserem auto ist, das bekommen wir hin indem wir ein 
messensor an die spize des Fahrzeuges befestigen.

(img Ampel)

Alsnächstes fügen wir unserem Start block 2 elemente hinzu 
1. eine Zeichen folge von midestens 2 Buchstaben und einer pause von 2sekunden (2000mili)
1. Eine Variable "fahrtautonom" die wir später noch brauchen werden also fügen wir setzte fahrtautonom auf 0

(img Start)

Jetzt beutzen wir die Variable, aber zuerst brauchen wir eine funktion "fallentscheidung" diese Funktion wird sagen ob 
wir grade selber fahren oder ob das auto selber fährt. In dieser funktion überprüfen wir das so: wenn fahrtautonom auf 
0 ist fahren wir selber wenn sie auf 1 ist fährt das Auto Selbständig. Dazu könen wir die funktion Autonom machen und 
ganz einfach sagen das die Motoren A und B auf 100 fahren, da es ja wegen der funktion "Ampelsystem"  gegen nichts 
fahren kann.

(img fallentscheidung)

Der aller letzteschritt ist das wir ein Signal empfangen und es deuten können/müssen (selber fahren oder Atonom)
dazu brauchen wir unter Funk den block datenpaket empafngen. In den Packen wir  2 mal den block wenn dann,
in den oberen fügen wir noch ein ansonsten hinzu, beim unteren nicht. Der Obere wird zum Selbersteuern benutz der untere
wird für das Autonome fahren gebraucht. Wenn das Signal= Autonom ist und unsere Variable "fahrtAutonom" 0 ist wird sie
au 1 gesetzt wenn sie auf 1 ist wird sie auf 0 gestezt,im klartext wenn man den befehl z.b durch drücken von B aktivirt
wird dem motor gesagt Autonom und wenn man nochmal B drückt wird Autonomes fahren außgeschaltet und man fährt von alleine 

(img datenemfang)


#
#####[lösung](https://github.com/Mcccake/calliope-car/blob/master/loesung.md)
