This method contains a self assignment of a local variable; e.g. public void foo() { int x = 3; x = x; }  Such assignments are useless, and may indicate a logic error or typo.