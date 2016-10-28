If you're a C# user in Visual Studio, you've probably noticed how quickly the using directives in a file can seem to get out of control. For those who may be unfamiliar with C#, more info on the directive can be found here: [using Directive](https://msdn.microsoft.com/en-us/library/sf0df423.aspx). For most users, using directives are added piecemeal, as needed, and generally have no real organization. To help manage this mess, Visual Studio has a set of features to organize usings. This problem focuses on a part of that featureset: "remove and sort". This feature both sorts the using directives alphabetically and removes any using directives that are not being used. To simplify this particular problem, the input will include a comment for each using directive indicating whether or not it is being used.

#### Input definition

The input will contain multiple sets of using directives, with each set terminated by the line "//----". Each using directive will be in the form "using <namespace>; //<comment>" where <namespace> will be a C# namespace and <comment> will be either "Used" or "Unused" to indicate if the using directive should be included.

#### Output definition

The output should contain the sorted and filtered sets of using directives, with each set terminated by the line "//----".

#### Example input

```
using System; //Used
using System.Text; //Unused
//----
using System.Collections.Generic; //Used
using System; //Unused
using System.Text; //Unused
using System.Threading.Tasks; //Unused
using System.Linq; //Used
//----
```
#### Example output

```
using System; //Used
//----
using System.Collections.Generic; //Used
using System.Linq; //Used
//----
```