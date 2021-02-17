# LUA---Covert-Date-String-To-Epoch

Converts a date string to epoch time and posts to QoS.

Use case - Replaces manual check to ensure no excess time skew on AS400 Server.  This script posts AS400 time in epoch to QoS.  Logmon runs a command posting epoch time on a Linux Server and the jdbc_response probe runs a SQL query which deducts one from the other - if great than 200 seconds - create alert.
