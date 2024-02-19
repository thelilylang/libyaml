# Update Lily modifications

Main commands to launch:

```sh
git reset --hard master # on lily_modifications branch
./bootstrap
./configure
mv include/config.h src
mv include/yaml.h src
echo "!src/config.h" >> .gitignore
```

Modification to be made to the `yaml_private.h` file.

```diff
diff --git a/src/yaml_private.h b/src/yaml_private.h
index b3351c4..f9b6d81 100644
--- a/src/yaml_private.h
+++ b/src/yaml_private.h
@@ -1,6 +1,4 @@
-#if HAVE_CONFIG_H
 #include "config.h"
-#endif

 #include <yaml.h>
```
