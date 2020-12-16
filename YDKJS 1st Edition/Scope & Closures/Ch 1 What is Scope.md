# You Don't know JS: Scope & Closures

## What is Scope?

1. **Scope** - a well defined set of rules for storing variables in some location
   and for finding those variables and a later time.

2. Any JS snippet is *compiled* before it is executed.

3. **Compilation process** - compiler goes though the declarations (var and functions)
   and registers them to accompaning scope(s).  
   Engine takes care og assignment/execution while consulting the accompaning scope
   for reference to any identifier.

4. If identifier is not found in scope - checks parent scope till global scope is reached.  
   If not found in gobal scope  
   
   - for read - Reference Error
   - for write - creates a new identifier in global scope (in non-strict mode)

5. Function decalration and fucntion expression assigned to a variable are treated
   differently by compiler. var refering to a fun expression is treated as a normal
   identifier, i.e the value stored n the var (i.e. the function) is not known to the 
   engine until the assignment statement is executed. => Function expressions are not hoisted.  
   
   
   Function decalrations are known to the engine to be *function* because the complier 
   not only adds the identifier to scope but also registers it as a fucntion value => they are hoisted.

6. Type Error - when read operation is successful by the engine => i.e. identifier
   is found in the scope (No Referenence Error) but you try to do something with the
   identifier that is not suitable for the type of the value in it. Example calling
   a non function value.
