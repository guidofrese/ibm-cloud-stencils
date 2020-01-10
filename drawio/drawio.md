## IBM VPC Stencils for draw.io

![VPCExperience](/images/vpc-experience-drawio.png)

# Implementation Notes

1. VPC stencils consists of:
    1. IBM / VPC (on draw.io)
    2. IBM / VPC Groups (VPCgroups.xml on this github)
    3. IBM / VPC Arrows (VPCarrows.xml on this github)
    4. Other IBM Icons
2. VPC Groups integrates the group tag (square icon in upper left corner) with the group border and also includes a few enhancements for consumability and readability.
3. Path of group tags at beginning of styles will change but current path will continue to be valid also.
4. Some group tags in VPC Groups won't initially match the example above.
5. Groups are implemented as containers except Security Group is not a container since it can span other groups. Containers are advantageous in that the contents are moved/copied along with the container.
6. VPC Icons include a standard version of networking icons by request such as load balancer, public gateway, VPN gateway, etc.  Other IBM icons for the same functionality may also be available such as the load balancer icon under Infrastructure.

# Upgrade Steps

To update an existing diagram to the latest version on this github for draw.io:
1. Make a local copy of VPCgroups.xml and VPCarrows.xml. 
2. Backup existing diagram, open existing diagram in draw.io, and enable Format Panel under View.
3. Under File select Open Library from Device... for VPCgroups.xml and VPCarrows.xml.
4. For each group in VPCgroups.xml: 
    1. Select group to temporarily add to canvas for extracting style.
    2. Select Edit Style (draw.io also provides Copy Style which copies the style but not the image settings).
    3. Select all of new style, right click, select Copy.
5. For each group in existing diagram: 
    1. For Subnet, move contents of ACL textbox to Subnet textbox, see example.
    2. Delete existing group tag.
    3. Select Edit Style (draw.io also provides Paste Style which along with Copy Style copies the style but not the image settings).
    4. Select all of old style, right click and select Delete, right click and select Paste to insert copied new style.
6. Similarly for arrows from VPCarrows.xml if desired.
7. Remove groups that were temporarily added to canvas.
8. If Cloud Universe group was used you can either leave as is or replace with the Public Network and Enterprise Network groups in VPCgroups.xml.
9. Tweek the diagram if more space is needed in places.

Return to [README](/README.md)