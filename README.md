# hvr
Action Reference 

Action 
Parameter 
Value 
Description 
Capture 
/IgnoreSessionName 
sess_name 
Capture changes directly from DBMS logging system 

/Coalesce 

Coalesce consecutive changes on the same row into a single change 

/NoBeforeUpdate 

Only capture the new values for updated rows 

/NoTruncate 

Do not capture truncate table statements 

/SupplementalLogging 
action 
Mechanism used to enable supplemental logging for SQL Server tables. 

/LogReadMethod 
method 
Method of reading SQL Server's transaction log. 

/LogTruncate 
action 
Specify who advances transaction log truncation point. 

/AugmentIncomplete 
col_type 
Capture job must select for column values. Can be NONE, LOB or ALL. 

/ArchiveLogPath 
dir 
Read archives from an alternative directory 

/ArchiveLogFormat 
format 
Format of base filename of archive files in directory /ArchiveLogPath 

/ArchiveLogOnly 

Capture data from archives only. Do not read from online redos 

/XLogDirectory 
dir 
Directory containing current PostgreSQL xlog files 

/LogJournal 
sch.jnl 
Specify DB2-for-i journal 

/TriggerBased 

Capture changes through generated DMBS triggers 

/QuickToggle 

Avoid shared lock on toggle table 

/ToggleFrequency 
secs 
Sleep between toggles instead of waiting for database alert (in seconds) 

/KeyOnlyCaptureTable 

Only keep keys in capture table; outer join others later 

/IgnoreCondition 
sql_expr 
Ignore changes that satisfy expression 

/IgnoreUpdateCondition 
sql_expr 
Ignore update changes that satisfy expression 

/HashBuckets 
int 
Hash structure to improve parallelism of captured tables 

/HashKey 
col_list 
Hash capture table on specific key columns 

/DeleteAfterCapture 

Delete file after capture, instead of capturing recently changed files 

/Pattern 
pattern 
Only capture files whose names match pattern 

/IgnorePattern 
pattern 
Ignore files whose names match pattern 

/IgnoreUnterminated 
pattern 
Ignore files whose last line does not match pattern 

/IgnoreSizeChanges 

Changes in file size during capture is not considered an error 

/AccessDelay 
secs 
Delay read for secs seconds to ensure writing is complete 

/UseDirectoryTime 

Check timestamp of parent dir, as Windows move doesn't change mod-time 
Integrate 
/Burst 

Resort changes, load into staging table and apply with set-wise SQL 

/BurstCommitFrequency 
freq 
Frequency of commits. Values STATEMENT, TABLE or CYCLE 

/Coalesce 

Coalesce consecutive changes on the same row into a single change 

/OrderByTable 

Sort changes to create a single file per table in a cycle 

/Resilient 
mode 
Resilient integrate for inserts, updates and deletes. Values WARNING or SILENT. 

/OnErrorSaveFailed 

Write failed row to fail table 

/DbProc 

Apply changes by calling integrate database procedures 

/TxBundleSize 
int 
Bundle small transactions for improved performance 

/TxSplitLimit 
int 
Split very large transactions to limit resource usage 

/NoTriggerFiring 

Enable/Disable triggering of database rules 

/SessionName 
sess_name 
Integrate changes with special session name sess_name 

/RenameExpression 
expression 
Expression to name new files, containing brace substitutions 

/ErrorOnOverwrite 

Error if a new file has same name as an existing file 

/MaxFileSize 
size 
Limit each XML file to size bytes 

/Verbose 

Report name of each file integrated 

/TableName 
apitab 
API name of table to upload attachments into 

/KeyName 
apikey 
API name of attachment table's key column 

/CycleByteLimit 
int 
Max amount of routed data (compressed) to process per integrate cycle 

/JournalRouterFiles 

Move processed router files to journal directory on hub 

/Delay 
N 
Delay integration of changes for N seconds 

/Context 
ctx 
Action only applies if Refresh/Compare context matches 
TableProperties 
/BaseName 
tbl_name 
Name of table in database differs from name in catalogs 

/DuplicateRows 

Table has duplicate rows and no unique key 

/Schema 
schema 
Database schema which owns table 

/IgnoreCoerceError 

Coerce illegal/big/small values to empty/max/min 

/TrimWhiteSpace 

Remove trailing whitespace from varchars 

/TrimTime 
policy 
Trim time when converting from Oracle and SqlServer date. 

/MapEmptyStringToSpace 

Convert between empty varchar and Oracle varchar space 

/MapEmptyDateToConstant 
date 
Convert between constant date (dd/mm/yyyy) and Ingres empty date 

/CreateUnicodeDatatypes 

On table creation use Unicode datatypes, e.g. map varchar to nvarchar 
ColumnProperties 
/Name 
col_name 
Name of column in hvr_column catalog 

/DatatypeMatch 
data_type 
Datatype used for matching instead of /Name 

/BaseName 
col_name 
Database column name differs from hvr_column catalog 

/Extra 

Column exists in base table but not in hvr_column catalog 

/Absent 

Column does not exist in base table 

/CaptureExpression 
sql_expr 
SQL expression for column value when capturing or reading 

/IntegrateExpression 
sql_expr 
SQL expression for column value when integrating 

/Key 

Add column to table's replication key 

/DistributionKey 

Distribution key column 

/SoftDelete 

Convert deletes to update of this column to 1. Value 0 means not deleted. 

/TimeKey 

Convert all changes to inserts, using this column for time dimension 

/IgnoreDuringCompare 

Ignore values in column during compare and refresh 

/Datatype 
data_type 
Datatype in database if it differs from hvr_column catalog 

/Length 
int 
String length in db if it differs from length in catalog 

/Precision 
int 
Precision in db if it differs from precision in catalog 

/Scale 
int 
Integer scale in db if it differs from scale in catalog 

/Nullable 

Nullability in db if it differs from nullability in catalog 

/Identity 

Column has SQL Server identity attribute 

/Context 
ctx 
Ignore action unless refresh/compare context ctx is enabled 
Restrict 
/CaptureCondition 
sql_expr 
Restrict during capture 

/IntegrateCondition 
sql_expr 
Restrict during integration 

/RefreshCondition 
sql_expr 
Restrict during refresh and compare 

/CompareCondition 
sql_expr 
Restrict during compare 

/HorizColumn 
col_name 
Horizontal partition table based on value in col_name 

/HorizLookupTable 
tbl_name 
Join partition column with horizontal lookup table 

/DynamicHorizLookup 

Changes to lookup table also trigger replication 

/AddressTo 
addr 
Only send changes to locations specified by address 

/AddressSubscribe 
addr 
Get copy of any changes sent to matching address 

/Context 
ctx 
Action only applies if Refresh/Compare context matches 
AdaptDDL 
/AddTablePattern 
patt 
Add new tables to channel if they match 

/IgnoreTablePattern 
patt 
Ignore new tables which match pattern 

/CaptureSchema 
db_schema 
Database schema for matching tables 

/IntegrateSchema 
db_schema 
Generate /Schema for target location(s) 

/RefreshOptions 
refr_opts 
Configure options for adapt's refresh of target 

/OnDropTable 
pol 
Behavior when source table dropped. Default: from channel only 

/KeepExistingStructure 

Preserve old columns in target, and do not reduce data types sizes 

/KeepOldRows 

Preserve old rows in target during recreate 
DbSequence 
/CaptureOnly 

Only capture db sequences, do not integrate them 

/IntegrateOnly 

Only integrate db sequences, do not capture them 

/Name 
seq_name 
Name of database sequence in HVR catalogs 

/Schema 
db_schema 
Schema which owns db sequence 

/BaseName 
seq_name 
Name of sequence in db if it differs from name in HVR 
CollisionDetect 
/TreatCollisionAsError 

Do not resolve collisions automatically 

/TimestampColumn 
col_name 
Exploit timestamp column col_name for collision detection 

/AutoHistoryPurge 

Delete history table row when no longer needed for collision detection 

/DetectDuringRefresh 
colname 
During row–wise refresh, discard updates if target timestamp is newer 

/Context 
context 
Action only applies if Refresh/Compare context matches 
DbObjectGeneration 
/NoCaptureInsertTrigger 

Inhibit generation of capture insert trigger 

/NoCaptureUpdateTrigger 

Inhibit generation of capture update trigger 

/NoCaptureDeleteTrigger 

Inhibit generation of capture delete trigger 

/NoCaptureDbProc 

Inhibit generation of capture database procedures 

/NoCaptureTable 

Inhibit generation of capture tables 

/NoIntegrateDbProc 

Inhibit generation of integrate database procedures 

/IncludeSqlFile 
file 
Search directory for include SQL file 

/IncludeSqlDirectory 
dir 
Search directory for include SQL file 

/CaptureTableCreateClause 
sql_expr 
Clause for trigger-based capture table creation statement 

/StateTableCreateClause 
sql_expr 
Clause for state table creation statement 

/BurstTableCreateClause 
sql_expr 
Clause for integrate burst table creation statement 

/FailTableCreateClause 
sql_expr 
Clause for fail table creation statement 

/HistoryTableCreateClause 
sql_expr 
Clause for history table creation statement 

/RefreshTableCreateClause 
sql_expr 
Clause for base table creation statement during refresh 
Transform 
/Command 
path 
Path to script or executable performing custom transformation 

/CommandArguments 
userarg 
Value(s) of parameter(s) for transform (space separated) 

/SapAugment 

Capture job selecting for de-clustering of multi-row SAP cluster tables 

/SapXForm 

Invoke SAP transformation for SAP pool and cluster tables 

/ExecOnHub 

Execute transform on hub instead of location's machine 

/Parallel 
n 
Distribute rows to multiple transformation processes 

/Context 
context 
Action only applies if Refresh/Compare context matches 
AgentPlugin 
/Command 
path 
Call OS command during replication jobs 

/DbProc 
dbproc 
Call database procedure dbproc during replication jobs 

/UserArgument 
str 
Pass argument str to each agent execution 

/ExecOnHub 

Execute agent on hub instead of location's machine 

/Order 
int 
Specify order of agent execution 

/Path 
dir 
Search directory dir for agent 
Environment 
/Name 
name 
Name of environment variable 

/Value 
value 
Value of environment variable 
FileFormat 
/Xml 

Transform rows form/into xml-files. Default 

/Csv 

Transforms rows from/into csv files 

/Avro 

Transforms rows into Apache AVRO format. Integrate only. 

/Compact 

Write compact XML tags like <r> & <c> instead of <row> & <column> 

/Compress 
algorithm 
Compress/uncompress while writing/reading. algorithm is GZIP or LZ4. 

/Encoding 
encoding 
Encoding of file 

/HeaderLine 

First line of file contains column names 

/FieldSeparator 
str_esc 
Field separator. Defaults to comma (,). Examples: , \\x1f or \\t 

/LineSeparator 
str_esc 
Line separator. Defaults to newline (\\n). Examples: ;\\n or \r\\n 

/QuoteCharacter 
str_esc 
Character to quote a field with, if the fields contains separators. Defaults to quote (\") 

/EscapeCharacter 
str_esc 
Character to escape the quote character with. Defaults to quote (\") 

/FileTerminator 
str_esc 
File termination at end-of-file. Example: EOF or \xff 

/AvroCompression 
codec 
Avro compression codec. Value should be Deflate. 

/AvroVersion 
version 
Version of Apache AVRO format. Possible values are v1_6, v1_7 and v1_8 (the default). 

/ConvertNewlinesTo 
style 
Write files with UNIX or DOS style newlines 

/CaptureConverter 
path 
Run files through converter before reading 

/CaptureConverterArguments 
userarg 
Arguments to the capture converter 

/IntegrateConverter 
path 
Run files through converter after writing 

/IntegrateConverterArguments 
userarg 
Arguments to the integrate converter program 

/Context 
context 
Action only applies if Refresh/Compare context matches 
LocationProperties 
/SslRemoteCertificate 
file 
Enable SSL encryption to remote location; verify location with certificate 

/SslLocalCertificateKeyPair 
path 
Enable SSL encryption to remote location; identify with certificate/key 

/ThrottleKbytes 
kbytes 
Restrain net bandwidth into packets of kbytes bytes 

/ThrottleMillisecs 
msecs 
Restrain net bandwidth by msecs second(s) wait between packets 

/StateDirectory 
path 
Directory for file location state files. Defaults to <top>/_hvr_state 

/CaseSensitiveNames 

DBMS table and columns names are treated case sensitive by HVR 

/Proxy 
proxy 
Proxy server URL for FTP, SFTP, WebDAV or Salesforce locations 

/Order 
N 
Specify order of hub->loc proxy chain 

/StagingDirectoryHvr 
URL 
Directory for bulk load staging files 

/StagingDirectoryDb 
URL 
Location for the bulk load staging files visible from the Database 

/StagingDirectoryCredentials 
credentials 
Credentials to be used for S3 authentication during RedShift bulk load 

/BulkAPI 

Use Salesforce Bulk API (instead of the SOAP interface). 

/SerialMode 

Force serial mode instead of parallel processing for Bulk API. 

/CloudLicense 

Location runs on cloud node with on-demand licensing, for example in Amazon or Azure Marketplace 
Scheduling 
/CaptureStartTimes 
times 
Trigger capture job at specific times, rather than continuous cycling 

/CaptureOnceOnStart 

Capture job runs for one cycle after trigger 

/IntegrateStartAfterCapture 

Trigger integrate job only after capture job routes new data 

/IntegrateStartTimes 
times 
Trigger integrate job at specific times, rather than continuous cycling 

/IntegrateOnceOnStart 

Integrate job runs for one cycle after trigger 

/RefreshStartTimes 
times 
Trigger refresh job at specific times 

/CompareStartTimes 
crono 
Trigger compare job at specific times 
