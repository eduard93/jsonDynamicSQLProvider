jsonDynamicSQLProvider
======================

Class for writing json from SQL Queries. Supports query parameters.

Installation.

1. Make Cachelib database read-write. (SMP → System Administration → Configuration → System Configuration → Local Databases, choose CACHELIB, uncheck Read Only, Save changes)
2. Import all files into SYS namespace
3. Compile classes ( %ZEN.Auxiliary.jsonDynamicSQLProvider )
4. Make Cachelib database read-only (optional but recommended, see 1 for how-to)

Usage example:
do ##class(%ZEN.Auxiliary.jsonDynamicSQLProvider).%WriteJSONFromDynamicSQL("json","SELECT Name,Age FROM Sample.Person WHERE Name=? And Age>?",$LB("John",60))

For details please refer to included documentation
