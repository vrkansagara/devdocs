---
layout: default
group: 
subgroup: 
title: Backward compatibility
menu_title: Backward compatibility
menu_order: 
github_link: extension-dev-guide/backward-compatibility.md
redirect_from: /guides/v1.0/extension-dev-guide/backward-compatibility.html
---
<h2>Backward compatibility</h2>

Merchants and developers want the process of upgrading between revisions of Magento 2 to be as easy as possible. For merchants, the process must be cost-effective, while developers want their extensions to be forward-compatible for as long as possible. 







<h3>What code is affected?</h3>
The backward compatibility policy applies to PHP code annotated with `@api`. This includes the following:

* Any interface used by third parties to enhance the system (payment providers, shipping providers, search providers).  We have sometimes called these SPIs.
* Individual methods or constants


<h3>Service Provider Interfaces</h3>



 





{% endhighlight %}


<h3>Versions</h3>

To reduce complexities, for Magento 2.0 GA, all components are versioned together. This does limit the value of our policy since a change in one module's public API affects the version of the entire set. Additionally, we expect to extract the `@api` PHP interfaces into a separate package, allowing more stability to third parties. Magento expects to be able to further reduce coupling of components after the 2.0 release.  


<h3>What other code changes can cause backward incompatibility?</h3>

Changes to the database can cause code to break.  As with PHP code, within a MAJOR version changes must be backward compatible. This means:









