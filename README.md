# Access Modifiers

In C#, **`access modifiers`** are keywords used to specify the visibility or accessibility of classes, methods, properties, and other members within a program. These modifiers control which parts of your program can access a particular member. C# has several access modifiers, each serving a different purpose. Here are the main access modifiers in C#:

1. **`Public (public)`**:

Members with the **`public`** access modifier are accessible from any other code in the same assembly or another assembly that references it.

Example:

```csharp
public class MyClass
{
    public int MyPublicField;
    public void MyPublicMethod() { }
}
```

2. **`Private (private)`**:

Members with the **`private`** access modifier are only accessible within the same class or struct.

Example:

```csharp
public class MyClass
{
    private int myPrivateField;
    private void MyPrivateMethod() { }
}
```

3. **`Protected (protected)`**:

Members with the **`protected`** access modifier are accessible within the same class or struct and by derived classes.

Example:

```csharp
public class MyBaseClass
{
    protected int MyProtectedField;
}

public class MyDerivedClass : MyBaseClass
{
    public void AccessProtected()
    {
        MyProtectedField = 10; // Accessing protected member from the base class
    }
}
```

4. **`Internal (internal)`**:

Members with the **`internal`** access modifier are accessible within the same assembly but not from other assemblies.

Example:

```csharp
internal class MyInternalClass
{
    internal int MyInternalField;
}
```

5. **`Protected Internal (protected internal)`**:

Members with the **`protected internal`** access modifier are accessible within the same assembly and by derived classes, even if they are in a different assembly.

Example:

```csharp
public class MyBaseClass
{
    protected internal int MyField;
}

// In a different assembly
public class MyDerivedClass : MyBaseClass
{
    public void AccessProtectedInternal()
    {
        MyField = 20; // Accessing protected internal member from a derived class in a different assembly
    }
}
```

6. **`Private Protected (private protected)`**:

Introduced in C# 7.2, the **`private protected`** access modifier is a combination of private and protected. It allows access within the same assembly by derived classes.

Example:

```csharp
public class MyBaseClass
{
    private protected int MyField;
}

public class MyDerivedClass : MyBaseClass
{
    public void AccessPrivateProtected()
    {
        MyField = 30; // Accessing private protected member from a derived class in the same assembly
    }
}
```

These access modifiers provide a way to control the visibility and accessibility of members, helping to encapsulate implementation details and enforce proper encapsulation in your code.
