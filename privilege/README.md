# Create file from the host
echo "I'm from the host" > greeting.txt
ls -la
exit
echo "Changes" > /root/greeting.txt

# Container priviledge
docker run -it -v /:/shared alpine sh
cd shared && vim /root/greeting.txt