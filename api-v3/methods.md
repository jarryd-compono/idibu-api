API v3 allows for six different methods of posting: ADD, UPDATE, QUICK REPOST, DELETE and CANCEL.

CANCEL, DELETE and QUICKREPOST have all different XML formats, suited to meet the needs of the information passed along.
ADD, UPDATE and REPOST

These 3 methods all share the same XML payload.

The difference between them is that both UPDATE and REPOST require an job id parameter to be passed in the JOB tag. If this id isn't in the payload, or the id doesn't correspond to a valid job id for the user, the request will fail.

For these 2 methods, the difference is that UPDATE works exactly as ADD, except that it works on a job that already exists in the system.

REPOST works in a similar fashion, with the difference that it completes the extra fields what the data already in the system, so there's no need to send all the extra fields for boards to which the job has already been posted. In that case all you need to do is send the board id and posting duration - sending the extra field data is optional.

You can find a detailed explanation here of all the tags that are used by these 3 methods.