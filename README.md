# sedonadev
Build sedonadev in Linux

# sedonadev
Build sedonadev in Linux

i) Download the latest sedonadev source code in below sedonadev site.

http://www.sedonadev.org/download/build/


ii) Unzip the sedonadev source.


iii) Install the JDK (Java development kit) in Linux Ubuntu host PC.

sudo add-apt-repository ppa:webupd8team/java

sudo apt-get update

sudo apt-get install oracle-java9-installer


iv) Edit the below file and change the "sedona_home" variable for sedonadev folder location and "java_home" location.

sedonadev/adm/unix/init.sh

Ex:
java_home=/usr/lib/jvm/java-9-oracle

sedona_home=/home/titus/workdir/sedonadev


v) Run the below command to export the build tools.

cd sedonadev

bash --rcfile adm/unix/init.sh 


vi) Build the svm using the below command.

makeunixdev


vii) Build scode and sab applications.

cd sedonadev

./bin/sedonac.sh scode/platUnix.xml

./bin/sedonac.sh apps/platUnix.sax