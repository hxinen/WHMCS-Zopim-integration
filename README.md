# WHMCS-Zopim-integration
When a WHMCS user logged in, it automatic fill in the firstname and e-mail


# Installation
1. You need ZOPIM Advanced(paid) because it use the ZOPIM API + first integrate ZOPIM widget into your WHMCS.
2. add the below code to your footer.tpl (/templates/yourtemplate/footer.tpl)


`	  {literal} <script> window.$zopim||(function(d,s){var z=$zopim=function(c){z._.push(c)},$=z.s= d.createElement(s),e=d.getElementsByTagName(s)[0];z.set=function(o){z.set. _.push(o)};z._=[];z.set._=[];$.async=!0;$.setAttribute("charset","utf-8"); $.src="//v2.zopim.com/?YOURKEY";z.t=+new Date;$. type="text/javascript";e.parentNode.insertBefore($,e)})(document,"script"); $zopim(function() { $zopim.livechat.setName('{/literal}{$clientsdetails.firstname}{literal}'); $zopim.livechat.setEmail('{/literal}{$clientsdetails.email}{literal}'); }); </script> {/literal}
`

3.  Replace `YOURKEY` with your ZOPIM key
 


