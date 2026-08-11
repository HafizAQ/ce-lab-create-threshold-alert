
# Install stress

sudo dnf install -y stress

# Generate CPU load (run for 15 minutes to trigger 2 evaluation periods)

stress --cpu 4 --timeout 900s

# Monitor in another terminal

watch -n 10 "aws cloudwatch describe-alarms --alarm-names HighCPUUtilization --query 'MetricAlarms[0].StateValue'"
