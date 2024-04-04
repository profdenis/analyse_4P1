# Diagramme de classes : Figures géométriques

## ShapesLib

[https://github.com/profdenis/shapes4p1](https://github.com/profdenis/shapes4p1)

### Diagramme de classes V1

````plantuml
@startuml
skinparam classAttributeIconSize 0
abstract class Shape {
  {static} +DefaultDrawColor : Color
  +DrawColor : Color
  +Shape()
  +Shape(Color)
  {abstract} +Draw(Canvas) : void
}

class Point {
  +X : int
  +Y : int
+Point(int, int)
+Point(int, int, Color)
+Point(Point)
+Draw(Canvas) : void
+Length() : int
}
Shape <|-- Point

class HLine {
+Width : int
+HLine(Point, int)
+HLine(Point, int, Color)
+HLine(HLine)
+Draw(Canvas) : void
}
Shape <|-- HLine
Point "1" <-- "*" HLine : start

class VLine {
+Height : int
+VLine(Point, int)
+VLine(Point, int, Color)
+VLine(VLine)
+Draw(Canvas) : void
}
Shape <|-- VLine
Point "1" <-- "*" VLine : start

class Line {
+Line(Point, Point)
+Line(Point, Point, Color)
+Line(Line)
+Draw(Canvas) : void
}
Shape <|-- Line
Point "2" <-- "*" Line : endpoints

class Triangle {
+Triangle(Point, Point, Point)
+Triangle(Point, Point, Point, Color)
+Triangle(Triangle)
+Draw(Canvas) : void
}
Shape <|-- Triangle
Point "3" <-- "*" Triangle : vertices

class Rectangle {
+Width : int
+Height : int
+Rectangle(Point, int, int)
+Rectangle(Point, int, int, Color)
+Rectangle(Rectangle)
+Draw(Canvas) : void
}
Shape <|-- Rectangle
Point "1" <-- "*" Rectangle : upperLeft

class Square {
+Width : int
+Square(Point, int)
+Square(Point, int, Color)
+Square(Square)
+Draw(Canvas) : void
}
Shape <|-- Square
Point "1" <-- "*" Square : upperLeft

class Circle {
+Radius : int
+Circle(Point, int)
+Circle(Point, int, Color)
+Circle(Circle)
+Draw(Canvas) : void
}
Shape <|-- Circle
Point "1" <-- "*" Circle : center

@enduml
````

[Sur PlantUML](https://www.plantuml.com/plantuml/dpng/ZPBFRjmW4CRlF0NQarqtKl_SgXnIRGwfj8SgMxdjaU396jMBNHYdKhVxxiLCPec58_bW6BvlO7w6kV6e78x7JlXVnWxAgQFKdVB-Cw8p3oF25ztRlVaByfrG3nwTqaWPSj-g0UH9I7aAfw3HPrdTmgCQExnrwi-sxtedFyauXwHgKOo756KAepEjJrpkJ5kBhR9FofTXzrDl6d4MWZY-ziPYvAX-13Cifl3dSrX5kmZVssbTpeGuK4NMurYAnPBL3km1swAaimC2tS7rlwihmc2ckvsn49YgxwR1bb6YIXK89fSOXvquBkFCoyT4GNUnUR-Hrq7RlDcG7dR4XsQycl7km1nQPBuwuyiavcEdNijNly9NB_4ntilYz32vnaXihGLwoVCXyJpZW6s6oVECzCqPPGzTnE9uXi64kRq8cx8uM0FDkGp-CO6pDUq3XqR3XVqUD9ANTUJi_IzvJ9uQ8VVoZaWf7AtvfqINTqVomivn6C3juF7I9VlVetBvFv4yQ-EaPTHiqRI6bp9pM38MIRV6QRhzUzMOqJCgwNDKrd9KjcXQWqgPEIeP4we6Y-343TXcF7R_0G00)

### Diagramme de classe V2

````plantuml
@startuml
skinparam classAttributeIconSize 0
abstract class Shape {
  {static} +DefaultDrawColor : Color
  +DrawColor : Color
  +Shape()
  +Shape(Color)
  {abstract} +Draw(Canvas) : void
}

class Point {
  +X : int
  +Y : int
+Point(int, int)
+Point(int, int, Color)
+Point(Point)
+Draw(Canvas) : void
+Length() : int
}
Shape <|-- Point

class HLine {
+Start : Point
+Width : int
+HLine(Point, int)
+HLine(Point, int, Color)
+HLine(HLine)
+Draw(Canvas) : void
}
Shape <|-- HLine

class VLine {
+Start : Point
+Height : int
+VLine(Point, int)
+VLine(Point, int, Color)
+VLine(VLine)
+Draw(Canvas) : void
}
Shape <|-- VLine

class Line {
+Start : Point
+End : Point
+Line(Point, Point)
+Line(Point, Point, Color)
+Line(Line)
+Draw(Canvas) : void
}
Shape <|-- Line

class Triangle {
+Vertex1 : Point
+Vertex2 : Point
+Vertex3 : Point
+Triangle(Point, Point, Point)
+Triangle(Point, Point, Point, Color)
+Triangle(Triangle)
+Draw(Canvas) : void
}
Shape <|-- Triangle

class Rectangle {
+UpperLeft : Point
+Width : int
+Height : int
+Rectangle(Point, int, int)
+Rectangle(Point, int, int, Color)
+Rectangle(Rectangle)
+Draw(Canvas) : void
}
Shape <|-- Rectangle

class Square {
+UpperLeft : Point
+Width : int
+Square(Point, int)
+Square(Point, int, Color)
+Square(Square)
+Draw(Canvas) : void
}
Shape <|-- Square

class Circle {
+Center : Point
+Radius : int
+Circle(Point, int)
+Circle(Point, int, Color)
+Circle(Circle)
+Draw(Canvas) : void
}
Shape <|-- Circle
@enduml
````

[Sur PlantUML](https://www.plantuml.com/plantuml/dpng/ZPHFJuCm6CRlV8eU8Mo9Vsx6mmmpcSaEPYZgiODkDBA2xSiqpdrtIzzqRSP8E8psVPwdzFTs3JC5L4AxgmBroKL39TsHlA9AFG18lcw1FUMrIFal8rS1NIkGD0TCaBIa3IE7W9230WeyFv9upZQqhM0kwNTILxKaTyICEXHV5CrBmiXDZTFL1xlT4PU62HLxgYAzUb_p8ZW60N8yrro0uOZVjQcBRlf1S1eREzI_ILT7vy84MKwwUUhgqfRnaeajb664xzO8U0RtVzCfObYcnP8BffdYj3jV7KStVkC5b9RCX713PEjBZWuTynoWysaGmD9a0pGBnhSbM9oiZvCDug2JZSN9V9m1caTHkCBR6AMehpaSjCR2-2mlabEnhGnFnYImdsi7WSBDkN3h1BlSntB4mxQ3zrDsCgO9cxMDh5WEfqvUcuR99TjSkddzFnwNUfZk1Wnx3jz5S3Qk0GliEaY_MYf7uMFIlwfzpG8w2uSnQ9YqN0cNEHvhmWGmwQ1MjE2jibIOywdwcgLo5WvZg30Pp9WekW_sFm00)

### Diagramme de classe V3

````plantuml
@startuml
skinparam classAttributeIconSize 0
abstract class Shape {
  {static} +DefaultDrawColor : Color
  +DrawColor : Color
  +Shape()
  +Shape(Color)
  {abstract} +Draw(Canvas) : void
}

class Point {
  +X : int
  +Y : int
+Point(int, int)
+Point(int, int, Color)
+Point(Point)
+Draw(Canvas) : void
+Length() : int
}
Shape <|-- Point

class HLine {
+Width : int
+HLine(Point, int)
+HLine(Point, int, Color)
+HLine(HLine)
}
Line <|-- HLine

class VLine {
+Height : int
+VLine(Point, int)
+VLine(Point, int, Color)
+VLine(VLine)
}
Line <|-- VLine

class Line {
+Start : Point
+End : Point
+Line(Point, Point)
+Line(Point, Point, Color)
+Line(Line)
+Draw(Canvas) : void
}
Shape <|-- Line

class Triangle {
+Vertex1 : Point
+Vertex2 : Point
+Vertex3 : Point
+Triangle(Point, Point, Point)
+Triangle(Point, Point, Point, Color)
+Triangle(Triangle)
+Draw(Canvas) : void
}
Shape <|-- Triangle

class Rectangle {
+UpperLeft : Point
+Width : int
+Height : int
+Rectangle(Point, int, int)
+Rectangle(Point, int, int, Color)
+Rectangle(Rectangle)
+Draw(Canvas) : void
}
Shape <|-- Rectangle

class Square {
+Square(Point, int)
+Square(Point, int, Color)
+Square(Square)
}
Rectangle <|-- Square

class Circle {
+Center : Point
+Radius : int
+Circle(Point, int)
+Circle(Point, int, Color)
+Circle(Circle)
+Draw(Canvas) : void
}
Shape <|-- Circle

@enduml
````

[Sur PlantUML](https://www.plantuml.com/plantuml/dpng/ZP9DxzCm3CRl-HGvjYf_YPSRuZ3K8Grf1xH2WQFNPcj4bvR47OYnxqxhu6MXOzfXYVFOwVEpbuL3i3WSMk6-QTE3XOEiMd3kBQBLsm7L-wepXVwbv7C1MuSMAlGLicYWL_8af3mv1DJLMMPBjOEXnQM57tdNTbQ-bhIFHTbDaJwIf26ap7G-iTtPNqroC4TmwNZxsEbQd8Nm71ywRP0uiYzZSZnCuTU_OKRfPFmzcyvf9D3Y7LcdDHKtBRErCdjiajH_UqJmCtZp--d9Op3JQgtDD9liiwwnOHHIoO5XPXBZS8RMT7IQTcz44XkLRBHIUjyWEvLpf_8_JfmfvqxbjHCR5GXsyl7zPkzC7GxN5Zp8M0l6d9gMs_EEvtlDyj5gCFkMU4fbKVrymH0ilFnNU1K4livOCV6zT80FLHmyqWJNSYCRLU6baqzzh-nQxS9qu-SJ_yMNgup9Ited5_132KUFD120kOFY-m2My2cA7rtGPW2SeetUNPW5EVa4s-JQLdvAkJAeR1ZH1cezE9wAhuiXM9j3S8gsX_htbMAXJ3qSsZy0)

### Diagramme de classe V4

````plantuml
@startuml

skinparam classAttributeIconSize 0

abstract class Shape {
{static} +DefaultDrawColor : Color
+DrawColor : Color
+Shape()
+Shape(Color)
{abstract} +Draw(Canvas) : void
}

class Point {
+X : int
+Y : int
+Point(int, int)
+Point(int, int, Color)
+Point(Point)
+Draw(Canvas) : void
+Length() : int
}
Shape <|-- Point

class HLine {
+Width : int
+HLine(Point, int)
+HLine(Point, int, Color)
+HLine(HLine)
}
Line <|-- HLine

class VLine {
+Height : int
+VLine(Point, int)
+VLine(Point, int, Color)
+VLine(VLine)
}
Line <|-- VLine

class Line {
+Start : Point
+End : Point
+Line(Point, Point)
+Line(Point, Point, Color)
+Line(Line)
+Draw(Canvas) : void
}
Shape <|-- Line

class Polygon {
+Polygon(...Point)
+Polygon(...Point, Color)
+Polygon(List<Point>)
+Polygon(List<Point>, Color)
+Polygon(Polygon)
+Draw(Canvas) : void
}
Shape <|-- Polygon
Point "3..*" <-o "*" Polygon : vertices

class Triangle {
+Vertex1 : Point
+Vertex2 : Point
+Vertex3 : Point
+Triangle(Point, Point, Point)
+Triangle(Point, Point, Point, Color)
+Triangle(Triangle)
}
Polygon <|-- Triangle

class Rectangle {
+UpperLeft : Point
+Width : int
+Height : int
+Rectangle(Point, int, int)
+Rectangle(Point, int, int, Color)
+Rectangle(Rectangle)
}
Polygon <|-- Rectangle

class Square {
+Square(Point, int)
+Square(Point, int, Color)
+Square(Square)
}
Rectangle <|-- Square

class Circle {
+Center : Point
+Radius : int
+Circle(Point, int)
+Circle(Point, int, Color)
+Circle(Circle)
+Draw(Canvas) : void
}
Shape <|-- Circle

@enduml
````

[Sur PlantUML](https://www.plantuml.com/plantuml/dpng/ZPDVRzCm5CNV_IciFIM4Hi3UK8M6EgGXzG6j4E3HIxpM8dMAVJF-b7vtdEkTkaggQG-pRy_ntU_urhtof1prsrRu7yRkb5DRMRVA-_T4pjprf3_MdLsPlrg-4aBTUNAgfdX4hZPgf-LUx3qfClL15jVwNlKjNJlrQz6rdPDl9U-YE2DnUvQZO3KNUq0EafkoXR8FokUXxw4pZJW84UcVEcCfq8jlmGgbABwZO2iBVo-7p_b824jaGUSr5sTnnLBRDMsoFFxlW8-tdl-RpM84vBbP6gk7F5zDGnj4OPK923EH40SEhtaW3Ni4iGHG1T2DDkiDWLHDI1C993ZLb5ITaW1QaN839zwt-62RzE4KWK6EDO1XCVRyl4_do_pqTRT_rfqTuZoMMLcM88wa18GJc9xcxBqxhqvR7lTd94Kw4H_bnMLPlhYGyradByAEwA5HEpArzhZKPsUKNRSyv2fu-lThJ1R2cx5mcGIqZsQDeJnXfm6bKoY61u78V3aOI7shQph6_hBRQRVKz-bzdFu0ne_qs8fCMF8dl9Gr7K4rJNjq47VrirUEit8r-esCjKI3nHjpqiMP50rW5iRLSIGBRKcxD8zRrPZUOmHyRXG2sZG4hBWzvod6a-9AswRVjly1)