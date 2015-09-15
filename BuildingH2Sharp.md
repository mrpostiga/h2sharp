# Introduction #

H2Sharp can be built on all the platforms supported by MonoDevelop.

However so far it seems to work well only on Microsoft .NET (hence, on Windows).

# Prequisites #

  * On Unix / MacOS X : Install [Mono](http://www.mono-project.com/Main_Page) and [MonoDevelop](http://monodevelop.com/)
  * On Windows : Install the free [Visual C# 2008 Express Edition](http://msdn.microsoft.com/fr-fr/express/aa975050.aspx) (not tested yet with [2010](http://www.microsoft.com/express/))
  * Install [IKVM.NET](http://www.ikvm.net/) and set the IKVM\_HOME environment variable to its main directory (should have a 'bin' sub-directory)

# Compiling H2Sharp #

  * [Checkout H2Sharp](http://code.google.com/p/h2sharp/source/checkout)
  * Open h2sharp/H2Sharp/H2Sharp.sln with MonoDevelop or Visual C++ and build

# Updating to a newer version of H2 #

  * Delete `h2sharp/H2Sharp/Dlls/*.jar`
  * Optional: put the version of h2.jar you want in the Dlls directory
  * Run the script `h2sharp/H2Sharp/CreateH2Dll.sh` : it will download the latest h2 JAR and convert all JARs in Dlls to DLL files
  * In Visual C++ or MonoDevelop, update the references to h2-xxx.dll in all the projects so that they point the newly generated h2-yyy.dll