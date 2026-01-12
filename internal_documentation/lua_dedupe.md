1. Implement new basic Lua event inside EventHandler, EventClient called `AddedDuplicateCommand`
2. Register event inside events.def - synced event, so we want to add MANAGED_BIT tag
3. Implement lua callin inside CLuaHandle (LuaHandle.cpp/h)
4. Fire it from game logic via eventHandler.CustomEvent(...)
5. Ensure it reaches correct Lua env (we want synced)