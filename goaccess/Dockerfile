FROM allinurl/goaccess

COPY ./apache2/access.log /debugAccess.log

RUN mkdir -p /var/log/apache2/

ENTRYPOINT ["/bin/sh", "-c"]

#CMD ["tail -f /dev/null"]
#CMD ["goaccess", "--dcf"]
#CMD ["cat", "/debugAccess.log"]
CMD ["goaccess /var/log/apache2/access.log -o /report/index.html --log-format=COMBINED --real-time-html -"]
#CMD ["goaccess", "/debugAccess.log -o /report.html --log-format=VCOMBINED --real-time-html -"]
#CMD ["goaccess", "/debugAccess.log -c"]
#CMD ["sleep", "infinity"]
#CMD ["tail", "-f", "/dev/null"]
