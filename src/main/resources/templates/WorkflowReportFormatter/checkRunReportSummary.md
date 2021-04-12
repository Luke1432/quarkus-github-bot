## <a id="build-summary-top"></a>Failing Jobs - Building {report.sha} - [Back to Pull Request]({pullRequest.htmlUrl})

| Status | Name | Step | Test failures | Logs | Raw logs |
| :-:  | --  | --  | :-:  | :-:  | :-:  |
{#for job in report.jobs}
{#if job.failing || (report.jvmJobsFailing && job.jvm)}
| {job.conclusionEmoji} | {job.name} | {#if job.failingStep}`{job.failingStep}`{/if} | {#if job.testFailuresAnchor}[Test failures](#user-content-{job.testFailuresAnchor}){#else if job.failing}:warning: Check →{/if} | {#if job.url}[Logs]({job.url}){/if} | {#if job.rawLogsUrl}[Raw logs]({job.rawLogsUrl}){/if}
{/if}
{/for}