<!--
title: 08 - Installing npm packages globally
featured: true
-->

# Installing npm packages globally

<iframe src="https://www.youtube.com/embed/JXi9pg5fsao" frameborder="0" allowfullscreen></iframe>

There are two ways to install npm packages: locally or globally. You choose which kind of installation to use based on how you want to use the package.

If you want to use it as a command line tool, something like the grunt CLI, then you want to install it globally. On the other hand, if you want to depend on the package from your own module using something like Node's `require`, then you want to install locally.

To download packages globally, you simply use the command `npm install -g <package>`, e.g.:

```
npm install -g jshint
```

If you get an EACCES error, you should login as the root or Administrator user and try again.  You can use `sudo`, but it's important to use the `-H` option to avoid getting EACCES errors later.  If you forget to use `-H` with `sudo`, you may have to [fix your permissions](/getting-started/fixing-npm-permissions).

Using `sudo` to install packages globally:

```
sudo -H npm install -g jshint
```

If you get errors due to proxy configuration *(happens because `http_proxy` is usually set for current user, and `sudo` uses `root`)*, give parameter `-E` to `sudo`.

```
sudo -E npm install -g jshint
```
