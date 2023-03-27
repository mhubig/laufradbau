# Laufradbau am Beispiel

Ich möchte hier am Beispiel der Laufräder für mein neues 650B Enduro MTB den
Aufbau eines MTB Laufradsatzes dokumentieren. Ich habe dafür folgende
Komponenten ausgewählt:

- Naben: [Hope Pro 2 EVO 40T][hopepro]
- Felgen: [WTB Frequency Team i25 650B][wtb-i25]
- Speichen: [Sapim D-Light][sapim-d] (2.0 - 1.65 - 2.0)
- Speichen: [Sapim Laser][sapim-l](2.0 - 1.5 - 2.0)
- Nippel: [Sapim Polyax][sapim-n] (14mm)

Die Kombination von D-Light und Laser Speichen soll einen belastungsgerechten
Aufbau der Laufräder ermöglichen. Dabei sollen die etwas stärkeren D-Light
Speichen immer auf der Seite mit dem steileren Speichenwinkel und der
dementbsprechend höheren Speichenspannung eingesetzt werden. Beide Laufräder
sollen mit dreifacher Kreuzung eingespeicht werden.

## 01. Berechnung der Speichenlänge

![Narbe Vermessen](http://fstatic1.mtb-news.de/f/ds/zn/dsznobro83i5/large_nabe-felge_vermessen.png?0)

Quelle: http://komponentix.de

Da moderne MTB-Naben meist asymetrisch gestaltet sind, kann die Länge der
Speichen auf jeder Laufradseite unterschiedlich sein und muss deshalb getrennt
berechnet werden. Um die korrekte Länge für eine Seite zu bestimmen werden
folgende Maße benötigt (hier beispielhaft für die Freilaufseite der Hope Nabe
Hinten rechts `Hr`):

0.  Abstand von Nabenmitte zur Nabenflanschmitte: `W_r=19mm`
1.  Nabenflansch Lochkreisdurchmesser: `d_r=54mm`
2.  Durchmesser Speichenloch: `s=2,6mm`
3.  Anzahl der Speichenkreuzungen: `x=3`
4.  Anzahl der Speichen: `n=16`
5.  Felgendurchmesser, gemessen am Nippelsitz: `ERD=565mm`

Die Maße der Hope Nabe stammen aus dem offiziellen [Hope Dokument][hopehub],
den (ERD) habe ich mit zwei auf (200mm) abgelängten Speichen gemessen,
bei denen ich die Nippel eingeklebt habe.

![Felge Vermessen](http://fstatic3.mtb-news.de/f/zt/sr/ztsro38qw28q/medium_MeasuringERD.png?0)

Quelle: http://komponentix.de

Hat man alle Maße bestimmt, kann die folgende Formel genutzt werden um die
Speichenlänge zu errechnen:

$$
S_L = \sqrt{
  \left(\frac{ERD}{2}\right)^2 +
  \left(\frac{d_r}{2}\right)^2 +
  \left(\frac{W_r}{2}\right)^2 -
  2 \cdot
  \left(\frac{ERD}{2}\right) \cdot
  \left(\frac{d_r}{2}\right) \cdot
  \cos{\frac{360^{\circ}}{n} \cdot x}
} - \frac{s}{2}
$$

Mit Hilfe dieser Formel konnten ich folgende Speichenlängen berechnen, welche
entsprechend gerundet diese reellen Speichenlängen ergeben.

```
Vorne Link:   272.44 mm -> 272 mm (D-Light)
Vorne Rechts: 273.99 mm -> 273 mm (Laser)
Hinten Links: 273.70 mm -> 273 mm (Laser)
Hinten Rechts 272.67 mm -> 272 mm (D-Light)
```

[hopepro]: http://www.hopetech.com/page.aspx?itemID=SPG241
[hopehub]: http://www.hopetech.com/webtop/modules/_repository/documents/2013HUBoffsetandpcd.pdf
[wtb-i25]: http://www.wtb.com/products/frequency-team
[sapim-d]: http://www.sapim.be/spokes/butted/d-light
[sapim-l]: http://www.sapim.be/spokes/butted/d-light
[sapim-n]: http://www.sapim.be/spokes/butted/d-light
