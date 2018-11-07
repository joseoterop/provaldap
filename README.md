# Examen LDAP

#### creador: jose otero perez

```
Servidor ldap con una base de datos llamada jose.cat donde se encuentran dos organizaciones llamadas
socis
simpatizantes
```
**Dentro de unidad socios de han insertado 3 personas**

#### Resumen de los inserts

```
Se han insertado 3 personalidades derivadas de inetOrgPerson creando un objeto llamado indepeOrgperson con los siguientes atributos:
Idcat
Sardanes
Lema
Twitter
la base de datos se indexa por Idcat
```
```
@@@ EJEMPLO @@@
dn: xidcat=1,ou=socis,dc=jose,dc=cat
objectclass: xindepeOrgPerson
objectclass: inetOrgPerson
cn: Pau codines
sn: pau
uid: 1
xidcat: 1
xsardanes: TRUE
xfoto: ///opt/docker/pedro.jpeg
xlema: viva sevilla
xtwitter: @elcoco

```
#### Se modifican a traves del fichero modi.ldif

```
Se modifan dos de las 3 personas introducidas y se les añade un objeto llamado llarenAccount
el cual tiene 3 atributos
Delictes
AnysCondemna
Galeres

```
```
@@@ EJEMPLO@@@
dn: xidcat=1,ou=socis,dc=jose,dc=cat
changetype: modify
add: objectClass
objectClass: xllarenaAccount
-
add: xdelictes
xdelictes: blasfemo
-
add: xgaleres
xgaleres: TRUE
-
add: xanyscondemna
xanyscondemna: 200

```
#### ACCESO AL CONTENIDO

```
DOCKERHUB: docker pull joterop/provaldap
GITHUB:https://github.com/joseoterop/provaldap

```

**DISCLAIMER: Cualquier parecido con nombres reales es pura casualidad.**
