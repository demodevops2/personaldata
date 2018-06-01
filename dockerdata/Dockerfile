FROM centos:6.8


# In case it isn't obvious, you do NOT need httpd, it is only
# an example implementation so can be safely ignored.
RUN yum -y install httpd; yum clean all;


# You HAVE to enable your service PRIOR to calling "init"
# since the init call is what ultimately fires it up
RUN service httpd start
RUN chkconfig httpd on

# Again, no need to expose port 80, it is used as part of the
# example implementation
EXPOSE 80
RUN echo "httpd" >> /root/.bashrc
CMD ["/bin/bash"]

