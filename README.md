## Script: Get Always On Cluster Configuration Details

**Description**:
This script queries `sys.dm_hadr_cluster` to retrieve details about the Windows Server Failover Cluster (WSFC) associated with the current SQL Server instance. It provides cluster-level metadata relevant to Always On Availability Groups.

**What It Shows**:
- Cluster name
- Quorum configuration and current quorum state
- Cluster type (WSFC or Distributed)
- Version and domain details (if applicable)

**Use Case**:
- Validate cluster settings when configuring or troubleshooting Always On AGs.
- Quickly confirm whether SQL Server is connected to a cluster.
- Useful for automation scripts during AG health checks.

**Requirements**:
- Always On feature must be enabled.
- SQL Server must be part of a WSFC.
- `VIEW SERVER STATE` permission is required.

**Notes**:
- Returns only one row per instance (cluster-level, not AG-level).
