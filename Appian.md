# Screening Round #

1. Asked to write possible parameters and methods for Alert system :- 

  My Ans:  alertId,alertName,alertMsg,Priority,Time

  Actual Ans:  alert_name,description,metric or log_filter,threshold,time_window,evaluation_interval,severity,notification_channels,recipients,tags
              
2. Asked to write code to retrieve first N alerts based on priority:-

  My Ans: I used priorityqueue to retreive based on priority
  AI Ans: 
   public static List<Alert> getTopNAlerts(List<Alert> alerts, int n) {
        // Sort alerts by priority ascending
        alerts.sort(Comparator.comparingInt(a -> a.priority));
        // Return first N alerts
        return alerts.subList(0, Math.min(n, alerts.size()));
    }
