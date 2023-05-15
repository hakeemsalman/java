# DataBase Connector Program in Java

```java
/*
 * 	DBTable : StudentDetails47
 *	(rollno,name,branch,totmarks,per,result)
 *	Prog-1 : Construct JDBC Application to read details from Console
 *	and insert into StudentDetails47.
 
 *	Read:
 *	rollno,name,branch,six sub marks
 
 *	Calculate:
 *	totMarks,per,result
 * 
    output:-
    ----------
    Please enter rollno.:
10
Please enter name:
wiah
Please enter branch name:
bio
Please enter Subject marks:
80
65
97
58
96
54
Thank you! Please wait
Marks calculated!
1 Record Inserted successfully!
-------------------------------------------------------
1  salman     mech       420      70.00    D 
1  salman     mech       397      66.17    D 
2  homd       ede        425      70.83    C 
5  shf        scs        1219     203.17   A 
6  home       it         256      42.67    fail 
10 wiah       bio        450      75.00    C 
---------------------------------------------------
 * 
 * 
 * 
 */
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.Statement;
import java.util.Scanner;

public class DBCon1 {
	public void creatingTable() {
		try {
			Scanner scan = new Scanner(System.in);
			Connection con = DriverManager.getConnection("jdbc:oracle:thin:@localhost:1521:xe", "salman", "tiger");
			Statement stm = con.createStatement();
			System.out.println("Please enter rollno.:");
			int rollno = scan.nextInt();
			System.out.println("Please enter name:");
			scan.nextLine();
			String name = scan.nextLine();
			System.out.println("Please enter branch name:");
			String branch = scan.nextLine();
			System.out.println("Please enter Subject marks:");
			int first = scan.nextInt();
			int second = scan.nextInt();
			int third = scan.nextInt();
			int forth = scan.nextInt();
			int fifth = scan.nextInt();
			int sixth = scan.nextInt();
			System.out.println("Thank you! Please wait");
			int totmark = first + second + third + forth + fifth + sixth;
			double percentage = 1.0 * totmark / 6;
			String result = "";
			if (percentage > 90) {
				result = "A";
			} else if (percentage > 80) {
				result = "B";
			} else if (percentage > 70) {
				result = "C";
			} else if (percentage > 60) {
				result = "D";
			} else
				result = "fail";
			System.out.println("Marks calculated!");
			int k = stm.executeUpdate("insert into StudentDetails  values('" + rollno + "','" + name + "','" + branch
					+ "','" + totmark + "','" + percentage + "','" + result + "')");
			if (k > 0) {
				System.out.println(k + " Record Inserted successfully!");
			} else
				System.out.println("Failed to insert!");

			ResultSet rs = stm.executeQuery("select * from StudentDetails");
			System.out.print("-------------------------------------------------------");
			while (rs.next()) {
				System.out.println();
				System.out.printf("%-2d %-10s %-10s %-8d %-8.2f %s ", rs.getInt(1), rs.getString(2), rs.getString(3),
						rs.getInt(4), rs.getFloat(5), rs.getString(6));

			}
			System.out.println();
			System.out.println("---------------------------------------------------");
			con.close();
			scan.close();

		} catch (Exception e) {
			e.printStackTrace();
		}
	}

	public static void main(String[] args) {

		new DBCon1().creatingTable();
	}
}
```
