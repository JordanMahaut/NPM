# Summary

- NPM Presentation
- Introducing NPX
- Node Packages
- Node Modules

## What's NPM (Node Package Manager)

NPM is an manager for Node Packages, used to publish packages and therefore share packages with other developpers using NPM<br>
NPM is divided by 3 axes.

1. NPM Website
    
    The [NPM](https://www.npmjs.com/) website is a usefull resource to see which packages are availables on the NPM Registry

2. CLI or Command Line Interface

    CLI's a very large part of NPM, because it's with CLI that you'll interact with NPM Registry.<br>
    You're able to download NPM packages from CLI, send yours, execute downloaded packages, so, it's a realy big part
    of NPM.

3. NPM Registry

    Registry is a huge database containing JS Packages, Registry can contain some JS applications or just some other packages
    That you'll be able to manage, adapt at your needs and so use in your own project.<br>
    But like it was said above, you can also get JS applications ready to use therefore, you can get applications and execute it

## What's NPX (Node Package Executer)

Like NPM is an manager for packages, NPX is an executer for packages.<br>
It means you're able to execute packages contained on NPM Registry without downloading them<br>
Note: You can also install packages with NPM and run them with NPM, but you'll need to download packages firstly

<br>

# Node Packages

An Node Package is a file or directory described in a **package.json** file
The json file will give some informations about package, that's why you have to add this **package.json** with the most detailled informations.
A Node Package can also be private or public [Read More About Package visibility](https://docs.npmjs.com/about-private-packages), and scoped or unscoped [Read More About Package scopes](https://docs.npmjs.com/about-scopes)

A node package can be all of following (And more) : 

1. A folder containing program described by **package.json**
2. An compressed file like .tgz (1.)
3. An URL resolving to (2.)
4. An GitHub URL that when cloned, resolve to (1.)

<br>

# Node Modules

An Node Module is a file or a directory placed in ``` node_modules ``` folder. <br>
Node Module is really powerful because you can able another developper using your module to work on his/her own code<br>
That way, you can write some code for other developpers.<br>
Node Module must be atleast one of following :

- An folder with **package.json** containing an ``` main ``` field
- A JS file

Node Modules are not required to have **package.json** so all modules arent packages. <br>
Node Modules are loaded by NodeJS function ``` require() ```

```js
let be_polite = require('hello_world_module');
```

In the code above, ``` be_polite ``` refers to ``` hello_world_module ```, be_polite will be an access point to 'hello_world_module'

<br>

# **package.json**

**package.json** as explained above is a file who'll be essential for your Node Package.<br>
This file can be compared to a map of your Package, you'll provides a lot of informations in.<br>
You'll put in followings informations (And again more) :

- name : How is called your package
- version : Version of current package
- description : Put an description to your package
- keywords : Pretty optionnal but if you want to share package with other developpers, it would be indispensable
- homepage : It can be a github repos or a Website, just the web referer to your package
- bugs : Where to report bugs, also can be a repos git to issues page
- author : Some information about you
- main : Used to entry point of your Node Module
- scripts : For advanced configuration of your package [Read More about script possibles values](https://docs.npmjs.com/cli/v8/using-npm/scripts)
- dependencies : To add a dependency at your project with version as value ``` "express":"4.18.2" ``` will add depency of express version 4.18.2 for example 
- devDependencies : To add a developpement depency on your package, see below
- private : true ; To be sure your package can't be published if you want to keep it private

And many others again. <br>

If you do not specify ``` scripts ``` for example, nmp will generate a default parameter, this way specifications arent required if you do not need to do specifics things.<br>


## Difference between Dependencies and devDependencies

To understand following, you need to understand truthely what's mean 'dependency'<br>
An dependency it a package that yours will need to work fine or just run (Depending of your code)<br>
If you're using express for example, you need to specify it in your **package.json** file, this way npm will ask for download express if user hasn't installated dependency. <br>

It's like trying open Microsoft PowerPoint on Linux. You arent able to get PowerPoint, so how can you be able to do a prensentation on. Just for example.<br>

So, when you put dependencies in your **package.json** file you're telling what your package will need to use to work fine. <br>

Now when you put devDependencies it's some dependencies to work on your package.<br>
For example, when you need to bake a cake, you need to get a furnace, setting up the furnace, etc<br>
And for eating the baked cake, you do not need a furnace just some other thing like, your mouth, a plate and optionnaly a flatware. <br>
It's the same principe, devDependencies will be used to bake the cake and dependencies will be used to eat the cake. <br>

====

Encore a faire, package-lock.json