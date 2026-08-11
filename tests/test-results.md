
# Check alarm state

aws cloudwatch describe-alarms 
  --alarm-names HighCPUUtilization 
  --query 'MetricAlarms[0].StateValue'
{
    "MetricAlarms": [
        {
            "AlarmName": "HighCPUUtilization",
            "AlarmArn": "arn:aws:cloudwatch:us-east-1:203637464233:alarm:HighCPUUtilization",
            "AlarmDescription": "Alert when CPU exceeds 80% for 10 minutes",
            "AlarmConfigurationUpdatedTimestamp": "2026-08-11T13:24:23.414000+02:00",
            "ActionsEnabled": true,
            "OKActions": [
                "arn:aws:sns:us-east-1:203637464233:CloudWatchAlerts"
            ],
            "AlarmActions": [
                "arn:aws:sns:us-east-1:203637464233:CloudWatchAlerts"
            ],
            "InsufficientDataActions": [],
            "StateValue": "INSUFFICIENT_DATA",
            "StateReason": "Unchecked: Initial alarm creation",
            "StateUpdatedTimestamp": "2026-08-11T13:24:23.414000+02:00",
            "MetricName": "CPUUtilization",
            "Namespace": "AWS/EC2",
            "Statistic": "Average",
            "Dimensions": [
                {
                    "Name": "InstanceId",
                    "Value": "i-03ca2f390a865bc9d"
                }
            ],
            "Period": 300,
            "EvaluationPeriods": 2,
            "Threshold": 80.0,
            "ComparisonOperator": "GreaterThanThreshold",
            "TreatMissingData": "notBreaching",
            "StateTransitionedTimestamp": "2026-08-11T13:24:23.414000+02:00"
        }
    ],
    "CompositeAlarms": []
}
(END)
            "Statistic": "Average",
            "Dimensions": [
                {
                    "Name": "InstanceId",
                    "Value": "i-03ca2f390a865bc9d"
                }
            ],
            "Period": 300,
            "EvaluationPeriods": 2,
            "Threshold": 80.0,
            "ComparisonOperator": "GreaterThanThreshold",
            "TreatMissingData": "notBreaching",
            "StateTransitionedTimestamp": "2026-08-11T13:24:23.414000+02:00"
        }
    ],
    "CompositeAlarms": []
}
(END)
"INSUFFICIENT_DATA"
