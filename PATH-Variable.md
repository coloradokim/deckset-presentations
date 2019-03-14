footer: kimschles
slidenumbers: true

# ⚡️ $PATH ⚡️

--- 
![inline](./images/dvlpdnvr.pdf)


--- 
![inline](https://res.cloudinary.com/kimschlesinger/image/upload/v1539033708/Call_for_partners_v2.png)


--- 

![inline](./images/RO-Logo-White.svg)

---
# Kim Schlesinger 


![inline 50%](http://res.cloudinary.com/kimschlesinger/image/upload/c_scale,w_2960/v1524009870/kimschlesinger-headshot.jpg)

---
# 👀
`echo $PATH` 

--- 
`/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin`

* Environment Variable
* 1 long string
* Colon-separated
* Is a path to executable code invoked through text commands

--- 
`/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin`

```
/usr/local/bin
/usr/bin
/bin
/usr/sbin
/sbin
```

---
# Editing $PATH

---
# Permanent Change

Add to .bashrc or right from the command line. 

`export PATH=$PATH:/Library/Frameworks/Python.framework/Versions/3.5/bin
`

--- 
# Temporary Change

From the command line. Only lasts in current shell (no export)

`PATH=$PATH:/Library/Frameworks/Python.framework/Versions/3.5/bin
`

--- 
# Recapitulation 
* Environment Variable
* 1 long string
* Colon-separated
* Is a path to executable code invoked through text commands

--- 
# Recapitulation

* See it with `echo $PATH`
* Change it with export: 

`export PATH=$PATH:/Library/Frameworks/new/thing`

* Try out a new path by taking out export: 

`PATH=$PATH:/Library/Frameworks/new/thing`

--- 
# Resources 

* [How to Access and Edit Path](https://truss.works/blog/2016/2/26/engineer-how-to-access-and-edit-your-path-system-variable) 
* [The /bin Directory
](http://www.linfo.org/bin.html) 

--- 
![inline](https://media.giphy.com/media/9Gp5ZwY8FRvna/giphy.gif)

kimschlesinger.com
hirediversity.us 

