# JasperReports-Hibernate5

Simple Java-library that consists of two classes and makes it possible to use JasperReports with 
Hibernate 5.

It can be built with maven by typing in command line:

mvn package

Built jar-package will be placed in target directory.


How-to-use
==========

1. The specified jar should be placed in project's library directory.
2. Change lines in property file *bold*default.jasperreports.properties*bold* in jasperreports*.jar:

Replace:

net.sf.jasperreports.query.executer.factory.hql=net.sf.jasperreports.engine.query.JRHibernateQueryExecuterFactory
net.sf.jasperreports.query.executer.factory.HQL=net.sf.jasperreports.engine.query.JRHibernateQueryExecuterFactory

with:

net.sf.jasperreports.query.executer.factory.hql=org.maxkreshch.jasperreports.engine.query.JRHibernate5QueryExecuterFactory
net.sf.jasperreports.query.executer.factory.HQL=org.maxkreshch.jasperreports.engine.query.JRHibernate5QueryExecuterFactory


