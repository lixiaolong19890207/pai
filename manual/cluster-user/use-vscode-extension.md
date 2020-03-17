# Use VSCode Extension

OpenPAI VS Code Client is an extension to connect OpenPAI clusters, submit AI jobs, simulate jobs locally, manage files, and so on.

## Connect to an OpenPAI cluster

Before using OpenPAI VS Code Client, follow below steps connecting to an OpenPAI cluster.

### Basic login

If you are using username and password to login to the cluster. Then you should follow this guide.

1. Use shortcut key <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> to open command palette.
2. Input and look for *PAI: Add PAI Cluster* as below.

    ![add cluster](https://raw.githubusercontent.com/Microsoft/pai/master/contrib/pai_vscode/assets/add_cluster.png)

3. Press <kbd>Enter</kbd>, and input the host of an OpenPAI cluster. It can be domain name or IP Address. After that, press <kbd>Enter</kbd> again.

    ![add cluster host](https://raw.githubusercontent.com/Microsoft/pai/master/contrib/pai_vscode/assets/add_cluster_host.png)

4. A configuration file is opened, and username and password fields are needed at least. Once it completes, click *Finish* button at right bottom corner. Notice, it won't be effect, if you save and close the file directly.

    ![add cluster configuration](https://raw.githubusercontent.com/Microsoft/pai/master/contrib/pai_vscode/assets/add-cluster-finish.png)

If there are multiple OpenPAI clusters, you can follow above steps again to connect with them.

### AAD login

If you are using AAD to login to the cluster. Then you should follow this guide.

1. Use shortcut key <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> to open command palette.
2. Input and look for *PAI: Add PAI Cluster* as below.

    ![add cluster](https://raw.githubusercontent.com/Microsoft/pai/master/contrib/pai_vscode/assets/add_cluster.png)

3. Press <kbd>Enter</kbd>, and input the host of an OpenPAI cluster. It can be domain name or IP Address. After that, press <kbd>Enter</kbd> again.

    ![add cluster host](https://raw.githubusercontent.com/Microsoft/pai/master/contrib/pai_vscode/assets/add_cluster_host.png)

4. If the `authn_type` of the cluster is `OIDC`, a webside will be open and ask you to login, after that a configuration file is opened, and if your login was successful the username and token fields are auto filled, you can change it if needed. Once it completes, click *Finish* button at right bottom corner. Notice, it won't be effect, if you save and close the file directly.

    ![add cluster configuration](https://raw.githubusercontent.com/Microsoft/pai/master/contrib/pai_vscode/assets/add_aad_cluster.gif)

If there are multiple OpenPAI clusters, you can follow above steps again to connect with them.

## Submit job

After added a cluster configuration, you can find the cluster in *PAI CLUSTER EXPLORER* pane as below.

![pai cluster explorer](https://raw.githubusercontent.com/Microsoft/pai/master/contrib/pai_vscode/assets/pai_cluster_explorer.png)

To submit a job yaml, please follow the steps below:

1. Double click `Create Job Config...` in OpenPAI cluster Explorer, and then specify file name and location to create a job configuration file.
2. Update job configuration as needed. If you are not familiar with this configuration file, learn from [here](https://github.com/microsoft/pai/blob/master/docs/marketplace-and-submit-job-v2/marketplace-and-submit-job-v2.md#introduction-to-yaml-file).
3. Right click on the created job configuration file, then click on `Submit Job to PAI Cluster`. The client will upload files to OpenPAI and create a job. Once it's done, there is a notification at right bottom corner, you can click to open the job detail page.

    If there are multiple OpenPAI clusters, you need to choose one.

    This animation shows above steps.
    ![submit job](https://raw.githubusercontent.com/Microsoft/pai/master/contrib/pai_vscode/assets/submit-job-v2.gif)


## Reference

  - [Full documentation of VSCode Extension](https://github.com/microsoft/openpaivscode/blob/master/README.md): Please note that, in the full documentation, two kinds of jobs are mentioned: V1 job and V2 job. You can safely skip contents about V1 job since it is deprecated.