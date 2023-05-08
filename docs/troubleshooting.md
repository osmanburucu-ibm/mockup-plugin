# MockUp

## Troubleshooting

### Copy Artifacts step limitation

When you use the Copy Artifacts step, you can copy only in the same logical partition (LPAR). To transfer artifacts between different LPARs, use the FTP Artifacts step.

### Missing return code for Run TSO or ISPF Command step

If you use the Run TSO or ISPF Command step to run a TSO command, the return code might not be displayed in IBM UrbanCode Deploy because the ISPF gateway does not support passing return codes when in TSO mode. To work around this behavior, in the **TSO Or ISPF** list, select **ISPF** instead of **TSO**.

### Repository field for Copy Artifacts and FTP Artifacts steps

The local repository referred to in the Copy Artifacts and FTP Artifacts steps is not the Codestation repository, but rather the z/OS deployment tools artifact repository. You specify this directory when you install the z/OS deployment tools. By default, the artifact repository is the following directory: *agent_installation_directory*/var/repository. To learn more, see [Completing the installation of the z/OS deployment tools](http://www-01.ibm.com/support/knowledgecenter/SS4GSP_6.2.1/com.ibm.udeploy.doc/topics/zos_installing_finish.html?lang=en).
