# Polymorhism

__Polymorphism is one of the core concepts of the OOP (Object Oriented Programming).__ Polymorphism is a word composed of two Greek words: _poly_, which means _many_, and _morph_, which means _forms_. Therefore, _polymorphism means many forms_. 

### <img src="https://user-images.githubusercontent.com/70295997/216810246-f805f12f-1176-4474-b5cb-cb24b0aa5d88.png" width=40> COMPILE-TIME Polymorphism / Method OVERLOADING
More precisely, in the OOP context, _polymorphism allows an object to behave differently in certain cases_, or, in other words allows an action to be accomplished  in different ways (approaches). _One way to implement polymorphism in Java is via method overloading. This is know as Compile-Time Polymorphism_ because the  compiler can identify at compile time which form of an overloaded method to call (multiple methods with the same name but different arguments). So, depending on which form of the overloaded method is called, the object behaves differently. For example, a class named <code>Triangle</code> can define multiple methods named <code>draw()</code> with different arguments.

<img src="https://user-images.githubusercontent.com/70295997/216810749-64a94f9b-00ad-4d5b-b112-2baa6157bb52.png" width=40>

    class Triangle {
        void draw() {
            System.out.println("Drawing a triangle");
        }

        void draw(String color) {
            System.out.println("Drawing a " + color + " triangle");
        }

        void draw(int width, int height) {
            System.out.println("Drawing a triangle with width " + width + " and height " + height);
        }
    }

    public class Main {
        public static void main(String[] args) {
            Triangle triangle = new Triangle();
            triangle.draw();
            triangle.draw("red");
            triangle.draw(10, 20);
        }
    }

Unlike many other popular object-oriented programming languages such as Java, Python doesn’t support compile-time polymorphism or method overloading. If a class or Python script has multiple methods with the same name, the method defined the latest overrides the earlier one.
Python doesn’t use function arguments for method signature, that’s why method overloading is not supported in Python.

<img src="https://user-images.githubusercontent.com/70295997/216810799-021871c1-780a-484d-8634-690968fe9c05.png" width=40> __Operator Overloading in Python__

Python supports operator overloading. This is another type of polymorphism where an operator behaves differently based on the type of the operands.
* operator multiplies two numbers and when used with a string and int, repeats the string given int times and concatenates them
* operator adds two numbers and concatenates two strings

The below snippet exhibits how to overload the <code>add</code> operator:

        class OperatorOverloading:
            def__init__(self, pages) :
                self.pages = pages

            def __add__(self, other):
                total_pages = self.pages + other.pages
                return total_pages

        obj1 = OperatorOverloading(10)
        obj2 = OperatorOverloading(5)
        print(obj1 + obj2)  # Output: 15

When changing <code>+</code> to <code>-</code> in the <code>total_pages</code> value definition, the result is subtraction in lieu of addition.

        class OperatorOverloading:
            def__init__(self, pages) :
                self.pages = pages

            def __add__(self, other):
                total_pages = self.pages - other.pages
                return total_pages

        obj1 = OperatorOverloading(10)
        obj2 = OperatorOverloading(5)
        print(obj1 + obj2)  # Output: 5

### <img src="https://user-images.githubusercontent.com/70295997/216810338-982cef29-ced4-4cfd-9cd5-072520812118.png" width=40> RUNTIME Polymorphism / Method OVERRIDING / Dynamic Dispatch

_Another way to implement polymorphism is via method overriding. This is a common approach where there's an IS-A relationship. It is known as Runtime Polymorhism, or Dynamic Dispatch._ Typically, we start with a parent interface/class containing a handful of methods. Next, each child class implements this parental interface/class and overrides these parental methods to provide a specific customized behavior. This time, polymorphism allows us to use any of these children classes exactly like its parent without any confusion of their types. This is possible because, at runtime, Java or Python is smart enough to distinguish among these classes and know which one is used. For example, an interface/class called <code>Shape</code> can declare a method named <code>draw()</code>, and the <code>Triangle</code>, <code>Rectangle</code>, and <code>Circle</code> classes implement the <code>Shape</code> interface/class and override the <code>draw()</code> method to draw the corresponding shape.

<img src="https://user-images.githubusercontent.com/70295997/216810799-021871c1-780a-484d-8634-690968fe9c05.png" width=40>

    class Shape:
        def draw(self):
            print("Drawing a shape")

    class Triangle(Shape):
        def draw(self):
            print("Drawing a triangle")

    class Rectangle(Shape):
        def draw(self):
            print("Drawing a rectangle")

    class Circle(Shape):
        def draw(self):
            print("Drawing a circle")

    def main():
        shapes = [Triangle(), Rectangle(), Circle()]
        for shape in shapes:
            shape.draw()

    if __name__ == '__main__':
        main()


### Advantages of Polymorphism
* The scripts and classes written once can be reused and implemented multiple times.
* It helps in reducing the coupling between different functionalities and behavior of objects.

<img width="800" src="https://user-images.githubusercontent.com/70295997/216844784-b7b015d0-d32f-4935-9267-cc75a4ac1c61.png">


[Inheritance](https://github.com/lana-20/oop-inheritance), another core OOP concept is essential in supporting Polymorphism in programming.
