# !bin/bash
mkdir git-source
cd git-source
read code
git clone $code
echo "cloning performed"
echo "performing build"
mvn -f pet_shop/pom.xml clean package -U
echo "build success"
echo "ssh connection "
ssh root@174.129.160.237
echo "deploying"
scp -r /root/git-source/pet_shop/target/petshop.war root@174.129.160.237:/root/apache-tomcat-9.0.83/webapps/
