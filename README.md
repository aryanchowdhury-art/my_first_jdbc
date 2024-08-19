# my_first_jdbc
it only check if the connections are working or not thats it

package com.jdbc;

import java.sql.*;

public class jdbcapp {
    public static void main(String[] args) {
        //this is our first jdbc project
        try {
            //load the driver to jdbc
            Class.forName("com.mysql.cj.jdbc.Driver");

            //creating a connection
            String url = "jdbc:mysql://localhost:3306/aryan";
            String username = "root";
            String password = "7075395094";
            Connection con=DriverManager.getConnection(url,username,password);

            if(con.isClosed()){
                System.out.println("the connections is still closed");
            }else {
                System.out.println("connection is created!!!");
                System.out.println("fuck yeah!!! you did it ...............");
            }

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
