# Arbitrary Stateful Operations in Structured Streaming of Spark

**GroupState.** Wrap around user-defined per-group state.

**Group.** Dataset.groupByKey() -> KeyValueGroupedDataset.

mapGroupsWithState: one group to one group

flatMapGroupsWithState: one group to many groups or none

ProcessingTime: System time, wall clock. 

* Can setTimeoutDuration.

EventTime: Time when events occurred. 

* Requires watermark. 
* setTimeoutTimestamp. Has to be newer than getCurrentWatermarkMs.

partition_interval is 1 day instead of 10 minutes for the dau case.

accumulate_interval: We need a dau count every 5 minutes. So the dau count would be accumulated distinct count.

When state timed out: For every timestamp: count the number of users that appeared before the timesatmp.

latestTimestampMs: Tracks up to which timestamp we have already output the result.

The state case class doesn't need to contain key, because it is handled under the hood.

Read the GroupState document.