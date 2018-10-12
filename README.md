# Graylog_dokcer

## --> Server Configuration from rsyslog

# vim /etc/rsyslog.d/graylog.conf
$template GRAYLOGRFC5424,”<%PRI%>%PROTOCOL-VERSION% %TIMESTAMP:::date-rfc3339% %HOSTNAME% %APP-NAME% %PROCID% %MSGID% %STRUCTURED-DATA% %msg%\n”
*.* @172.31.8.130:514

# systemctl restart rsyslog
