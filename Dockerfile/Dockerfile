FROM ubuntu                            #ubuntu image
WORKDIR /tmp                           #working directoy tmp
RUN echo "Hello World" > testfile.txt  #command run on create image
ENV myname pratik                      #create environment variable with name myname and value pratik
COPY testfile1 /tmp                    #copy from local machine to docker image
ADD test.tar.gz /tmp                   #like copy command
