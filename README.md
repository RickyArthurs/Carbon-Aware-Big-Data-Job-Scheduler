# Carbon-Aware-Big-Data-Job-Scheduler
This implementation is a carbon aware scheduler that can be deployed on a cluster, which successfully reduces the carbon footprint of jobs submitted.

This was my fourth year project at the University of Glasgow.

To begin scheduling jobs the jobSubmissionTool should be started first using the following command
```console
python jobSubmissionTool.py
```
This will then prompt the user for job submissions

To start the scheduler run the following command
```console
python scheduler.py
```
After executing this command the scheduler will process the job queue present and offset jobs based on carbon intensity predictions

The scheduler will maintain this queue making real-time updates to execution times based on improved forecasts

The system is currently configured to be ran on a Google Cloud Platform cluster, this can be reconfigured for any other cloud provider
this can be done by changing the only interaction with the cluster on line 37 of the scheduler i.e. the spark-submit command.

The logs text file will keep track of jobs which are submitted the cluster, the information for the job profile will be appended to the logs along with the execution time