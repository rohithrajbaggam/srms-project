# Major Project

## Student management system

### **Technologies Used**

```python
Java 
MySQL
Java Swing
```

## Tools

```python
Apache NetBeans (Code editor)
```

### Create New Project in Net Beans

- New Project
- Java With Ant → Java Application

## Note

```python

* Ant
* Maven
* Gradle

These are the 3 frameworks provided by Apache. These are the toolbars helps to building the projects.

⇒Maven is a project management tool. Maven is a dependency management and a build automation tool, primarily used for Java applications.

⇒ Ant is a Java library used for automating build processes for Java applications.

⇒ Gradle is a dependency management and a build automation tool that was built upon the concepts of Ant and Maven.
```

## MySQL

We are using mysql as your database

### Commands For SQL

- `mysql -u root -p`   is used to start SQL server in terminal
- `create database srm;` is used to create a new database
- `use srm;`   if we have multiple databases we use this to change run selected database by entering
- `create table tableName;`  to create a table inside database

```sql
create table student(name varchar(30), rollno varchar(20) primary key, 
gender varchar(30), fathername varchar(30), course varchar(40), 
branch varchar(40));
```

### mysql-connector-j-8.0.31.jar

[MySQL :: Download Connector/J](https://dev.mysql.com/downloads/connector/j/?os=26)

- It supports the Java Database Connectivity (JDBC).
- We need to add jar file inside library to use inside the project.
- We need to call driver class which is `com.sql.cj.jdbc.Driver` to initialise JDBC connectivity.

## JDBC Connection

```java
try{
		Class.forName("com.mysql.cj.jdbc.Driver");
		Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/srm", "root", "Rohihani#4264");
}
catch (SQLException | ClassNotFoundException ex) {
		JOptionPane.showMessageDialog(null, ex.toString());
}
```

## Insert Command

```java
try {
            // TODO add your handling code here:
            String name = jTextField1.getText();
            String rollno = jTextField2.getText();
            String gender = (String) jComboBox1.getSelectedItem();
            String fathername = jTextField3.getText();
            String course = (String) jComboBox2.getSelectedItem();
            String branch = (String) jComboBox3.getSelectedItem();

        Class.forName("com.mysql.cj.jdbc.Driver");
        Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/srm", "root", "Rohihani#4264");
        
        Statement st = connection.createStatement();
        st.executeUpdate("insert into student(rollno, course, branch, name, gender, fathername) values('"+rollno+"', '"+course+"', '"+branch+"', '"+name+"', '"+gender+"', '"+fathername+"' )");
        JOptionPane.showMessageDialog(null, "Data added Successfully !");
        setVisible(false);
        new index().setVisible(true);
                 
       } 
cath (SQLException | ClassNotFoundException ex) {
            JOptionPane.showMessageDialog(null, ex.toString());
    }
```

### RS2XML.JAR FILE

[](https://sourceforge.net/projects/finalangelsanddemons/files/rs2xml.jar/download)

- In our project RS2XML.jar file is used  to display the data in a table format
- After downloading jar file we need to add to library in our project.

[Celery](https://www.notion.so/Celery-e3c6a004113c4c5ca692468a912079b8)