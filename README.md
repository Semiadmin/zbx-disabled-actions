# zbx-disabled-actions
I think many have come across this feature of Zabbix:
"If a certain object (host, template, trigger, etc.) used in an action condition/operation is deleted, the condition/operation is removed and the action is disabled to avoid incorrect execution of the action. The action can be re-enabled by the user."
https://www.zabbix.com/documentation/current/en/manual/config/notifications/action/conditions#actions-disabled-due-to-deleted-objects
It is sad that this is happening without any warning and without recording in the audit.
This simple template will help you notice the problem to fix it or confirm it by manually closing a trigger.
Macros {$ZABBIX.ROOT.URL} and {$API.TOKEN} are not set in the template because they are supposed to be used as global macros.
