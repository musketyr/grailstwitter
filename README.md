# grailstwitter
Deployment to AWS Beanstalk Demo using Grails Twitter Sample Application


## JAR Deployment
You can see changes needed to deploy as JAR in following commit

https://github.com/musketyr/grailstwitter/commit/5d166f5a882b768649c2581971b03e9d19b52cfc

You need to create appropriate application and environment with type _Web Server / Java_, set the AWS credentials either as environmental
variables or using `~/.aws/credentials`and than run `gradle deployStaging`.

Don't forget to set environment variable `PORT` to `8080`, otherwise you will not be able to connect to the application.

## JAR Deployment with Zip Archive
Elastic Beanstalk allows you to add additional configurations inside `.ebextensions` directory inside deployed archive. In that case you
need to pack your JAR file into zip archive along with the `.ebextensions` directory. See following commit for steps which needs to be
performed on top of the previous step:

https://github.com/musketyr/grailstwitter/commit/c986d01e851d2a91888dbd19ec0037a61fd97600
