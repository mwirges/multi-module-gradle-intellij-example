Let's say you have module A and B that are not normally a multi-module gradle project.

Let's also say you want IntelliJ to treat B as a compile dependency of A for running or test A.

Normally you have to do something like [this](http://stackoverflow.com/a/23279998).

Instead if you create a bogus multi-module project using this settings.gradle and build.gradle, it will automatically include your subprojects as modules and IntelliJ will link the modules as compile dependencies instead of having to do it manually.

This is basically to work-around this: https://youtrack.jetbrains.com/issue/IDEA-151558#tab=Comments

The example here is dirty and of course could be improved.
