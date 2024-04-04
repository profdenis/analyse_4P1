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