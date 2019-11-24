Odoo Java Api
================

This reppo is no longer maintained for new odoo versions. https://github.com/odoo-java/odoo-java-api is the appropriate project for improvements.
Current issues and PR will be maintained on the new repo.

A Java API to connect to Odoo and manage data using the XMLRPC interface.

The API reduces the amount of boiler plate code needed to communicate with Odoo 
by doing error checking and type conversions.

The Api IS known to work for :
* openerp-java-api-1.3.0 works perfectly up to OpenERP v7
* openerp-java-api-2.0.x si supposed to work with the new API introduced in odoo v8
** Take care, the package name have replace openerp by odoo so that compatibility is broken
* openerp-java-api-3.0.x , package renamed, tested on Odoo v10
** purposed is to be pushed on maven for pentaho integration

For more information, including a Wiki please see the project on SourceForge: 
[https://sourceforge.net/projects/openerpjavaapi/](https://sourceforge.net/projects/openerpjavaapi)

The project is realeased under the Apache V2 license starting from version 1.5.  
Earlier versions are dual licenced and developers can choose between LGPL3 (original license) and Apache V2.


# Dependencies

This project depends on the XMLRPC library by Apache: http://ws.apache.org/xmlrpc

Download the latest version from apache and extract the tar.

The required jar files are:
xmlrpc-client-3.1.3.jar
xmlrpc-common-3.1.3.jar
ws-commons-util-1.0.2.jar

Add those jar files to your classpath and you should be ok.

# Examples

## Context manipulation
			Map inputMap = new java.util.HashMap();
			inputMap.put("active_id", move_id.toString());
			openERPSession.getContext().putAll(inputMap);
