# POSIX Compatibility of CFS

CFS adopts [pjdfstest](https://github.com/pjd/pjdfstest/tree/master/) to ensure the POSIX compatibility.

## Experiment Setup

* Linux 3.10.0
* Centos 6.3
* CephFS 12.2.5

## Test Result
We first printed the mount points for Ext4, XFS and CFS, and then start pjdfstest, respectively.
![](https://github.com/cfs-for-review/CFS-for-review/blob/main/figures/ext4_xfs_cfs.png)
The results show that both Ext4 and CFS passed all 8832 testcases, while XFS failed 2 test cases.

We additionally evaluate the CephFS, and the result shows that it failed 237 test cases.
![](https://github.com/cfs-for-review/CFS-for-review/blob/main/figures/cephfs.png)
