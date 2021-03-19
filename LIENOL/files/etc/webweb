#!/bin/sh

if [ -n "$(ls -A "/gzip/gzip_1.10-3_x86_64.ipk" 2>/dev/null)" ]; then
  opkg install /gzip/gzip_1.10-3_x86_64.ipk  --force-depends
fi
sed -i 's/<%=pcdata(ver.distversion)%>/<%=pcdata(ver.distversion)%><!--/g' /usr/lib/lua/luci/view/admin_status/index.htm
sed -i 's/(<%=pcdata(ver.luciversion)%>)/(<%=pcdata(ver.luciversion)%>)-->/g' /usr/lib/lua/luci/view/admin_status/index.htm
sed -i '/webweb/d' /etc/crontabs/root
rm -rf /gzip
rm -rf /etc/webweb
