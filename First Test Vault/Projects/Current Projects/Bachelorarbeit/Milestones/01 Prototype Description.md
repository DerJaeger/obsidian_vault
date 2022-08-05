#Bachelorarbeit 
#ba_01_prototype

# Description
This step should establish the first part of the Project.
Goal is a working Protoype which
+ Can Analyse Bug Reports and associate the Traceback calls to corospoding files.
+  Identify through SVN which developer was last changing this file.
	+ During last release phase?
	+ Last n devs which changes the file?
	+ Should dev leader also get a notification

# Stucture Idea
SVN Container which has multiple users already edited a known file structure.

Bug Report Sorter which gets an input of known Bug Reports and links them to files and identifies responsible.

The Bug Report Sorter is called manually

The Sorter only cares about where the error originates from, not in which files the functions which throws the error gets called.

The Bug Reports are inputed as an file like Yaml, Json or plain text and get processed in order.

The output is the name of the bugreport and to which developers it is send


A Bug Report complies to the following structure:

Name: <name>
Date: <yyyy-mm-dd>
(Version: <version>)
Customer: <customer_name>
Operating System: <os_type>
Report: <traceback-call>

The Traceback call is structured as follows:

<path_to_origin_file> <function_name> <error_type>
<path_to_other_file> <function_name> <error_type>
<path_to_other_file_2> <function_name> <error_type>


# Open Questions

+ When to update source file db

