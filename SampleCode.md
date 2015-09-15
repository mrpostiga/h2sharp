# Introduction #

Here is a simple sample of code using H2Sharp

# Code #

```
using System;
using System.Data.H2;

namespace H2SharpExample
{
    public class Program
    {
        static void Main(string[] args)
        {
            using (H2Connection connection = new H2Connection("jdbc:h2:~/test", "sa", ""))
            {
                connection.Open();
                using (H2Command command = connection.CreateCommand())
                {
                    command.CommandText = "Select 'hello world'";
                    Console.WriteLine(command.ExecuteScalar());
                }
            }
        }
    }
}
```

# References #

You will have to add a reference to the H2Sharp dll. If you use anything in the API namespace you will have to also reference the h2.dll. Whether you reference them or not you will still have to have the h2 dll, the ikvm.net dlls and the class library dll in the directory for the program.

# More advanced examples #

See http://code.google.com/p/h2sharp/source/browse/trunk/H2Sharp/H2Examples/Main.cs