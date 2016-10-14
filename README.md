##to check high volume usage folders in GB
du -h | sort -hr | head -30
##sts credentials generation
aws sts assume-role --role-arn arn:aws:iam::123456789012:role/role-name --role-session-name "RoleSession1" --profile IAM-user-name > /tmp/assume-role-output.txt
export AWS_ACCESS_KEY_ID=AKIAI44QH8DHBEXAMPLE
export AWS_SECRET_ACCESS_KEY=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
export AWS_SECURITY_TOKEN=AQoDYXdzEJr...<remainder of security token>
##Command to check number of hits
cat /var/log/apache2/access.log | awk '{print $1}' | sort -n | uniq -c | sort -nr
##all files & sizes
find / -size +10000k -exec ls -sd {} +
