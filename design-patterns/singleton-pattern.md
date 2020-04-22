# The Singleton Pattern

The Singleton pattern can be implemented by creating a class with a method that creates a new instance of the class if one doesn't exist. In the event of an instance already existing, it simply returns a reference to that object.

Singletons differ from static classes (or objects) as we can delay their initialization.

>It is neither the object or "class" that's returned by a Singleton, it's a **structure**.

Singletons serve as a shared resource namespace which isolate implementation code from the global namespace so as to provide a single point of access for functions.
