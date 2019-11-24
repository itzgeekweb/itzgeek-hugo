+++
title = "Install Cacti On Debian 10"
subtitle = ""
description = "Cacti is an open source network monitoring tool designed as the front end application for the RRDtool. It allows users to poll services at an interval of time and resulting in a graph format."

# Add a summary to display on homepage (optional).
summary = "CentOS 8 was reeased on September 24th, 2019 by the CentOS Project. It is derived from RHEL 8 which was released on May 7th, 2019."


date = 2019-06-23T07:53:53Z
lastmod = 2019-10-04T07:53:53Z
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Raj"]

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["centos-8"]
categories = ["CentOS"]

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
# projects = ["internal-project"]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
[image]
  # Caption (optional)
  caption = "Install Cacti On Debian 10"

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++
<strong><a href="https://www.cacti.net/" rel="nofollow">Cacti</a></strong> is an open source network <strong><a href="/tag/monitoring-tools">monitoring tool</a></strong> designed as the front end application for the RRDtool. It allows users to poll services at an interval of time and resulting in a graph format.

<strong><a href="/tag/cacti">With Cacti</a></strong>, you can get a graph for CPU and network bandwidth utilization. Also, it monitors the network traffic by polling a router or switch via <strong><a href="/tag/snmp">SNMP</a></strong>.

Here is the post about <strong><a href="/tag/cacti">installing Cacti</a></strong> on <strong><a href="/tag/debian-9">Debian 9</a></strong>.
<h2><span style="text-decoration: underline; color: #800000;">Requirements</span></h2>
Switch to the root user.
<pre>su -</pre>
<strong>OR</strong>
<pre>sudo  su -</pre>
Update the repository index.
<pre>apt-get update</pre>
Install below packages for cacti installation.
<pre>apt-get -y install apache2 php php-mysql php-snmp mariadb-server mariadb-client snmpd rrdtool
</pre>
<h2><span style="text-decoration: underline; color: #800000;">Install Cacti</span></h2>
Install the cacti package using the apt-get command.
<pre>apt-get -y install cacti</pre>
Follow the onscreen instruction for setting up Cacti.

Select the web server and press enter to configure the web server for Cacti automatically. By doing this, Cacti eases our web server configuration you do it for accessing Cacti web interface.

In my case, the web server is <strong>apache2</strong>.

[caption id="attachment_25805" align="aligncenter" width="970"]<img class="size-full wp-image-25805" src="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Webserver-for-Cacti.png" alt="Install Cacti on Debian 9 - Webserver for Cacti" width="970" height="414" /> Install Cacti on Debian 9 - Webserver for Cacti[/caption]

Click <strong>Yes to configure a database</strong> for cacti or <strong>click No to set up a database manually</strong>.

[caption id="attachment_25806" align="aligncenter" width="1024"]<a href="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Create-Database-for-Cacti.png"><img class="size-large wp-image-25806" src="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Create-Database-for-Cacti-1024x348.png" alt="Install Cacti on Debian 9 - Create Database for Cacti" width="1024" height="348" /></a> Install Cacti on Debian 9 - Create Database for Cacti[/caption]

Enter the <strong>password for Cacti user</strong> for <strong>cacti database</strong>. <strong>This password is also for Cacti Web Interface</strong>.

[caption id="attachment_25807" align="aligncenter" width="1024"]<a href="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Confirm-DB-user-password.png"><img class="wp-image-25807 size-large" src="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Confirm-DB-user-password-1024x269.png" alt="Install Cacti on Debian 9 - Set a Password for DB user" width="1024" height="269" /></a> Install Cacti on Debian 9 - Set a Password for DB user[/caption]

Reenter the password.

[caption id="attachment_25808" align="aligncenter" width="1024"]<a href="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Set-a-Password-for-DB-user.png"><img class="size-large wp-image-25808" src="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Set-a-Password-for-DB-user-1024x282.png" alt="Install Cacti on Debian 9 - Confirm DB user password" width="1024" height="282" /></a> Install Cacti on Debian 9 - Confirm DB user password[/caption]
<h2><span style="text-decoration: underline; color: #993300;">Configure Cacti</span></h2>
In <strong><a href="/tag/debian-9">Debian 9</a></strong>, you do not need to setup Cacti or go through the series of installation procedure over a web interface.
<h2><span style="text-decoration: underline;"><span style="color: #993300; text-decoration: underline;">Access Cacti</span></span></h2>
Open up a browser and visit the below URL.
<div class="itzgeek-url">http://your.ip.add.ress/cacti</div>
Login to Cacti using username "<strong>admin</strong>" and <strong>the password you entered during database setup</strong>.

[caption id="attachment_25814" align="aligncenter" width="916"]<a href="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Cacti-Login-Page.png"><img class="size-full wp-image-25814" src="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Cacti-Login-Page.png" alt="Install Cacti on Debian 9 - Cacti Login Page" width="916" height="460" /></a> Install Cacti on Debian 9 - Cacti Login Page[/caption]
<h3><span style="color: #000080;">Reset Cacti admin password (Optional)</span></h3>
If you are still unable to login to Cacti web interface then follow below steps.

Log in Cacti database with the user <strong>cacti</strong> and the password you entered during the Cacti installation.
<pre>mysql -u root -p cacti</pre>
Run the following <strong><a href="/tag/mysql">MySQL</a></strong> query. Replace <strong>yourpassword </strong>with the password of your choice.
<pre>update user_auth set password=md5('<span style="color: #00ff00;"><strong>yourpassword</strong></span>') where username='<span style="color: #00ff00;"><strong>admin</strong></span>';</pre>
The <strong>Cacti Dashboard </strong>will look like below after successful login.<strong>
</strong>

[caption id="attachment_25815" align="aligncenter" width="914"]<a href="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Cacti-Dashboard.png"><img class="size-full wp-image-25815" src="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Cacti-Dashboard.png" alt="Install Cacti on Debian 9 - Cacti Dashboard" width="914" height="698" /></a> Install Cacti on Debian 9 - Cacti Dashboard[/caption]

<strong>Usage graph of a device (localhost):</strong>

[caption id="attachment_25816" align="aligncenter" width="997"]<a href="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Cacti-Graph.png"><img class="size-full wp-image-25816" src="https://www.itzgeek.com/wp-content/uploads/2017/09/Install-Cacti-on-Debian-9-Cacti-Graph.png" alt="Install Cacti on Debian 9 - Cacti Graph" width="997" height="722" /></a> Install Cacti on Debian 9 - Cacti Graph[/caption]

Now you can add devices to Cacti and monitor its usage. More documentation can be found <strong><a title="Cacti Documentation" href="http://www.cacti.net/documentation.php" rel="nofollow">here</a></strong>.

That's All.
