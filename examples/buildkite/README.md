# Secret

Create ssh key
```bash
kubectl create secret generic ssh-key-secret --from-file=id_rsa=/path/to/.ssh/id_rsa --from-file=id_rsa.pub=/path/to/.ssh/id_rsa.pub --from-file=config=/path/to/.ssh/config
```

# External metrics

```
% kubectl get --raw="/apis/external.metrics.k8s.io/v1beta1/" -A  | jq -r ".resources[].name" | sort                                           (git)-[master]
buildkite_busy_agent_count
buildkite_busy_agent_percentage
buildkite_idle_agent_count
buildkite_running_jobs_count
buildkite_scheduled_jobs_count
buildkite_total_agent_count
buildkite_total_busy_agent_count
buildkite_total_busy_agent_percentage
buildkite_total_idle_agent_count
buildkite_total_running_jobs_count
buildkite_total_scheduled_jobs_count
buildkite_total_total_agent_count
buildkite_total_unfinished_jobs_count
buildkite_total_waiting_jobs_count
buildkite_unfinished_jobs_count
buildkite_waiting_jobs_coun
```