a Pluggable Database (PDB) is a self-contained database within an Oracle Container Database (CDB).
PDBs allow multiple databases to share resources while acting independently.

The following are queries and their ScreenShoot

SQL> CREATE PLUGGABLE DATABASE plsql_class2024db
  2  ADMIN USER hu_plsqlauca IDENTIFIED BY sqlplus
  3  ROLES = (DBA)
  4  FILE_NAME_CONVERT = ('C:\app\king\product\21c\oradata\xe\pdbseed\',
  5                       'C:\app\king\product\21c\oradata\xe\plsql_class2024db\');

Pluggable database created.


![image](https://github.com/user-attachments/assets/e8a042eb-6271-410c-a4c1-008be7df028f)


=======================================================================================================================


SQL> CONNECT SYS AS SYSDBA;
Enter password:
Connected.
SQL> ALTER PLUGGABLE DATABASE plsql_class2024db OPEN;

Pluggable database altered.

![PDB2](https://github.com/user-attachments/assets/daf1d49b-f7e8-49a4-86d7-376c34f3d949)

=======================================================================================================================

SQL> CREATE PLUGGABLE DATABASE hu_to_delete_pdb
  2  ADMIN USER hu_plsqlauca2 IDENTIFIED BY sqlplus
  3  ROLES = (DBA)
  4  FILE_NAME_CONVERT = ('C:\app\king\product\21c\oradata\xe\pdbseed\',
  5                       'C:\app\king\product\21c\oradata\xe\hu_to_delete_pdb\');

Pluggable database created.
![PDB_Delet](https://github.com/user-attachments/assets/1e0acfb1-b014-4a71-ac16-88e4cc33cbc4)

===============================================================================================================================
![PDB_Removed](https://github.com/user-attachments/assets/76f0d4fd-d7ef-4ca6-acdb-ba63f71b1908)


