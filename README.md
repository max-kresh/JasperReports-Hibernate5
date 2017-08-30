# JasperReports6-Hibernate5

Simple Java-library that consists of two classes and makes it possible to use JasperReports with 
Hibernate 5.

About
=====
Basically, it's two sligthly amended classes from JasperReports library:

**net.sf.jasperreports.engine.query.JRHibernateQueryExecuterFactory**
**net.sf.jasperreports.engine.query.JRHibernateQueryExecuter**

How-to-build
============

It can be built with maven by typing in command line:

`mvn package`

Built jar-file will be placed in **target** directory.


How-to-use
==========

1. The specified jar should be placed in project's libraries directory.
2. Change lines in file **default.jasperreports.properties** in **jasperreports\*.jar**:

**Replace:**

```
net.sf.jasperreports.query.executer.factory.hql=net.sf.jasperreports.engine.query.JRHibernateQueryExecuterFactory
net.sf.jasperreports.query.executer.factory.HQL=net.sf.jasperreports.engine.query.JRHibernateQueryExecuterFactory
```

**With:**

```
net.sf.jasperreports.query.executer.factory.hql=org.maxkreshch.jasperreports.engine.query.JRHibernate5QueryExecuterFactory
net.sf.jasperreports.query.executer.factory.HQL=org.maxkreshch.jasperreports.engine.query.JRHibernate5QueryExecuterFactory
```

