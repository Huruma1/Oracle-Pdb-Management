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


=======================================================================================================================

SQL> CREATE PLUGGABLE DATABASE hu_to_delete_pdb
  2  ADMIN USER hu_plsqlauca2 IDENTIFIED BY sqlplus
  3  ROLES = (DBA)
  4  FILE_NAME_CONVERT = ('C:\app\king\product\21c\oradata\xe\pdbseed\',
  5                       'C:\app\king\product\21c\oradata\xe\hu_to_delete_pdb\');

Pluggable database created.
