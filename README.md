This is in relation to a use-case that I get asked about a lot and this is in relation to backing up PVs (Persistent Volumes) from one cluster to another.  This type of operation is good if you want to have a hot-standby site to fail-over to in the event of maintenance or some type of disaster.

There are multiple ways to tackle this problem.  There is the OADP (Openshift Application Data Protection) Operator, there are ways to do this with ODF (Openshift Data Foundations) Disaster Recovery tooling, and some third-party solutions.  The reason I am covering VolSync is because it is more light-weight than the ODF solution and doesn't require a full ODF cluster.  In addition, this is part of ACM (Advanced Cluster Management) that I've been writing about recently.

In this article, the following topics will be covered:

A.  Installing VolSync add-on

B.  Setting up Metal-LB (more on this later)

C.  Setting up ReplicationDestination CRD on Spoke2

D.  Setting up ReplicationSource CRD on Spoke2

E.  Mounting this as permanent volume in case of Disaster/Maintenance

https://github.com/kcalliga/volsync
https://www.myopenshiftblog.com/acm-add-ons-volsync-and/
