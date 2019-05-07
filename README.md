# ![LOGO](logo.png) Crucible **flow**ground Connector

## Description

A generated **flow**ground connector for the Crucible API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/crucible.local/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:40:09+03:00

## API Description



## Authorization

This API does not require authorization.

## Actions

### Get the user authentication token.<br/>
>  <br/>
>  This is a legacy version of the login request. Using GET is deprecated as your password is likely to appear in logs which record request URLs.<br/>
>  Use the POST version instead.

#### Input Parameters
* `userName` - _optional_ - the username of the user to get the token for
* `password` - _optional_ - the password for the user to get the token for

### Get the user authentication token.

### Get the list of projects that the authenticated user is entitled to access.

#### Input Parameters
* `excludeAllowedReviewers` - _optional_ - if set to true, user data (e.g. allowedReviewers) which is expensive
 to compute, will not be included in the response data. Defaults to false so allowedReviewers are included in the response.

### Returns a project description.

#### Input Parameters
* `excludeAllowedReviewers` - _optional_

### Returns a list of all repositories. This includes plugin provided repositories

#### Input Parameters
* `name` - _optional_ - filter repositories by the repository key, only repositories of keys containing this value
 would be returned if value was provided.  Case insensitive.
* `enabled` - _optional_ - filter repositories by enabled flag.  Only enabled/disabled repositories would be returned
 accordingly if value was provided.
* `available` - _optional_ - filter repositories by its availability.  Only available/unavailable repositories would be returned
 accordingly if value was provided.
* `type` - _optional_ - filter repositories by type.  Allowed values: cvs, svn, p4, git, hg, plugin (for light SCM repositories).
 Parameter can be specified more than once.
* `limit` - _optional_ - maximum number of repositories to be returned.

### Lists the contents of the specified directory.

#### Input Parameters
* `path` - _required_ - path to a directory. When path represents a file name, the result is unspecified.
* `repository` - _required_ - the key of the Crucible SCM plugin repository.

### Represents a particular changeset.

#### Input Parameters
* `repository` - _required_ - the key of the Crucible SCM plugin repository.
* `revision` - _required_ - the SCM revision string.

### Represents a sorted list of changesets, newest first.

#### Input Parameters
* `oldestCsid` - _optional_ - only return change sets after this change set. If omitted there is no restriction.
* `includeOldest` - _optional_ - include the change set with id "from" in the change sets returned.
* `newestCsid` - _optional_ - only return change sets before this change set. If omitted there is no restriction.
* `includeNewest` - _optional_ - include the change set with id "to" in the change sets returned.
* `max` - _optional_ - return only the newest change sets, to a maximum of maxChangesets.

### Returns the raw content of the specified file revision as a binary<br/>
>  stream. No attempt is made to identify the content type and no mime<br/>
>  type is provided.

#### Input Parameters
* `path` - _required_ - the path of a file.
* `repository` - _required_ - the key of the Crucible SCM plugin repository.
* `revision` - _required_ - the SCM revision string.

### Represents the history of a versioned entity.

#### Input Parameters
* `path` - _required_ - the path of a file or versioned directory (note that
 versioned directories are not supported by all SCM plugins).
* `repository` - _required_ - the key of the Crucible SCM plugin repository.
* `revision` - _required_ - the SCM revision string.

### getRepositoryDetails

#### Input Parameters
* `repository` - _required_ - the key of the Crucible SCM plugin repository.

### For backward compatibility we provide this method, but repositories should be referred to just by their key.

#### Input Parameters
* `repository` - _required_ - the key of a FishEye or Crucible SCM plugin repository

### details

#### Input Parameters
* `path` - _required_ - the path of a file or versioned directory (note that
 versioned directories are not supported by all SCM plugins).
* `repository` - _required_ - the key of the Crucible SCM plugin repository.
* `revision` - _required_ - the SCM revision string.

### getAllReviews

#### Input Parameters
* `state` - _optional_ - only return reviews that are in these states.

### createReview

### Retrieves all reviews that are in one of the the specified states. For each review all details are included (review items + comments). The<br/>
>  wiki rendered comments will be available via the <messageAsHtml> element

#### Input Parameters
* `state` - _optional_ - the review states to match.

### To ignore a property, omit it from the query string.

#### Input Parameters
* `title` - _optional_ - a string that will be searched for in review titles.
* `author` - _optional_ - reviews authored by this user.
* `moderator` - _optional_ - reviews moderated by this user.
* `creator` - _optional_ - reviews created by this user.
* `states` - _optional_ - comma-separated list of amy of the following strings: (Draft,
 Approval, Review, Summarize, Closed, Dead, Rejected, Unknown).
* `reviewer` - _optional_ - reviews reviewed by this user.
* `orRoles` - _optional_ - whether the value of , ,
  and  should be OR'd
 () or AND'd ()
 together.
* `complete` - _optional_ - reviews that the specified reviewer has completed.
* `allReviewersComplete` - _optional_ - Reviews that all reviewers have completed.
* `project` - _optional_ - reviews for the specified project.
* `fromDate` - _optional_ - reviews with last activity date after the specified timestamp, in milliseconds. Inclusive.
* `toDate` - _optional_ - reviews with last activity date before the specified timestamp, in milliseconds. Inclusive.

### This method should no longer be used, as it uses a POST for a read-only<br/>
>  retrieval operation and is provided for backward compatibility only.

### To ignore a property, omit it from the query string.

#### Input Parameters
* `title` - _optional_ - a string that will be searched for in review titles.
* `author` - _optional_ - reviews authored by this user.
* `moderator` - _optional_ - reviews moderated by this user.
* `creator` - _optional_ - reviews created by this user.
* `states` - _optional_ - comma-separated list of amy of the following strings: (Draft,
 Approval, Review, Summarize, Closed, Dead, Rejected, Unknown).
* `reviewer` - _optional_ - reviews reviewed by this user.
* `orRoles` - _optional_ - whether the value of , ,
  and  should be OR'd
 () or AND'd ()
 together.
* `complete` - _optional_ - reviews that the specified reviewer has completed.
* `allReviewersComplete` - _optional_ - Reviews that all reviewers have completed.
* `project` - _optional_ - reviews for the specified project.
* `fromDate` - _optional_ - reviews with last activity date after the specified timestamp, in milliseconds. Inclusive.
* `toDate` - _optional_ - reviews with last activity date before the specified timestamp, in milliseconds. Inclusive.

### This method should no longer be used, as it uses a POST for a read-only<br/>
>  retrieval operation and is provided for backward compatibility only.

### Get all the reviews which match the given filter, for the current user.

#### Input Parameters
* `filter` - _required_ - a predefined filter type.

### Gets a list of all the reviews that match the specified filter criteria.

#### Input Parameters
* `filter` - _required_ - a predefined filter type.

### Get comment metrics metadata for the specified metrics version.

#### Input Parameters
* `version` - _required_ - a metrics version.

### Return a list of Reviews which include a particular file.

#### Input Parameters
* `path` - _optional_ - path to find in reviews

### Return a list of Reviews which include a particular file.

#### Input Parameters
* `path` - _optional_ - path to find in reviews.

### Returns Crucible version information.

### Permanently deletes the specified review.<br/>
>  The review must have been abandoned.

#### Input Parameters
* `id` - _required_ - the permId of the review to delete (e.g. "CR-45").

### Get a single review by its permId (e.g. "CR-45").<br/>
>  If the review does not exist, a 404 is returned.<br/>
>  <br/>
>  The moderator element may not exist if the review does not have a Moderator.

#### Input Parameters
* `id` - _required_ - the permId of the review to delete (e.g. "CR-45").

### Get a list of the actions which the current user is allowed to perform<br/>
>  on the review.

#### Input Parameters
* `id` - _required_ - the permId of the a review (e.g. "CR-45").

### addChangesetToReview

#### Input Parameters
* `id` - _required_ - the perm id of the review to add the changeset to

### addFile

#### Input Parameters
* `id` - _required_ - the review perma id to add the file

### Old, non-restful name. Kept for backwards compatibility. Exactly the same as POSTing to /{id}/patch

#### Input Parameters
* `id` - _required_

### Closes the given review with the summary given.

#### Input Parameters
* `id` - _required_ - the review perma id to close. it should be in the open state.

### Return all the comments visible to the requesting user for the review.

#### Input Parameters
* `render` - _optional_ - indicate whether to render the wiki text in the returned comments. If set to "true", the comments will contain a
 <messageAsHtml> element containing the wiki rendered html.

### Add a general comment to the review.

#### Input Parameters
* `id` - _required_ - the review perma-id

### getGeneralComments

#### Input Parameters
* `render` - _optional_ - indicate whether to render the wiki text in the returned comments. If set to "true", the comments will contain a
 <messageAsHtml> element containing the wiki rendered html.

### For the effective user, mark all comments in a review as read (except<br/>
>  those marked as leave unread).

#### Input Parameters
* `id` - _required_ - the review perma-id (e.g. "CR-45").

### getVersionedComments

#### Input Parameters
* `render` - _optional_ - indicate whether to render the wiki text in the returned comments. If set to "true", the comments will contain a
 <messageAsHtml> element containing the wiki rendered html.

### Deletes the given comment.

#### Input Parameters
* `id` - _required_ - the perma id of the review
* `cId` - _required_ - the id of the comment

### Gets the given comment.

#### Input Parameters
* `render` - _optional_ - true if the wiki text should be rendered into html, into the field <messageAsHtml>.
* `cId` - _required_ - the id of the comment

### Updates the comment given by the perma id to the new comment posted.

#### Input Parameters
* `id` - _required_ - the perma id of the review
* `cId` - _required_ - the id of the comment

### Marks the comment as leave unread to the current user - it will not automatically be marked as read by crucible.

#### Input Parameters
* `id` - _required_ - the review perma id for the comment
* `cId` - _required_ - the comment perma id

### Mark the given comment as read for the user used to make this POST.

#### Input Parameters
* `id` - _required_ - the review perma id
* `cId` - _required_ - the comment perma id.

### Gets the replies to the given comment.

#### Input Parameters
* `render` - _optional_ - true if the comments should also be rendered into html, into the element <messageAsHtml>
* `cId` - _required_ - the comment to reply to

### Adds a reply to the given comment. This call includes the  repsonse header that<br/>
>  contains the URL of the newly created entity.

#### Input Parameters
* `id` - _required_ - the review perma-id (e.g. "CR-45").
* `cId` - _required_ - the comment to reply to

### Deletes the reply.

#### Input Parameters
* `id` - _required_ - The review perma id
* `rId` - _required_ - the perma id of the reply to delete
* `cId` - _required_ - the reply's parent comment perma id

### Updates a reply with the given newComment.

#### Input Parameters
* `id` - _required_ - The review perma id
* `rId` - _required_ - the perma id of the reply to delete
* `cId` - _required_ - the reply's parent comment perma id

### Completes the review for the current user

#### Input Parameters
* `ignoreWarnings` - _optional_ - if {@code ignoreWarnings==true} then condition failure warnings will be ignored

### Returns the specified review.

#### Input Parameters
* `id` - _required_ - the permId of the review (e.g. "CR-45").

### Get a list of patches and their details for the given review

#### Input Parameters
* `id` - _required_ - the review id to get the patches for

### Add the revisions in a patch to an existing review.

#### Input Parameters
* `id` - _required_ - the review id to get the patches for

### Removes the patch with the given id from the review. All of the revisions provided by the patch will be removed as well.

#### Input Parameters
* `patchId` - _required_ - the id of the patch (as returned by the '{id}/patch' resource)
* `id` - _required_ - the permaId of the review

### Publishes all the draft comments of the current user.

#### Input Parameters
* `id` - _required_ - the review perma id to look for draft comments

### publishes the given draft comment.

#### Input Parameters
* `id` - _required_ - the review perma id
* `cId` - _required_ - the comment perma id

### Immediately send a reminder to incomplete reviewers about the given review.

#### Input Parameters
* `id` - _required_ - the review perma id to remind about. it should be in the open state.

### Get a list of reviewers in the review given by the permaid id.

#### Input Parameters
* `id` - _required_ - the id of the review to add to

### Adds the given list of reviewers to the review.

#### Input Parameters
* `id` - _required_ - the id of the review to add to

### Gets a list of completed reviewers.

#### Input Parameters
* `id` - _required_ - the review perma id to retrieve reviewers

### Gets a list of reviewers that have not completed the review.

#### Input Parameters
* `id` - _required_ - the review perma id to retrieve reviewers

### Removes the reviewer from the review.

#### Input Parameters
* `id` - _required_ - the perma id of the review
* `username` - _required_ - the name of the reviewer.

### Returns a list of all the items in a review.

#### Input Parameters
* `id` - _required_ - the id of the review (e.g. "CR-362").

### Add the changes between two files in a fisheye repository to the review.

#### Input Parameters
* `id` - _required_ - the id of the review (e.g. "CR-362").

### Adds the given review item to the review. This will always create a new review item, even if there is an existing<br/>
>  one with the same data in the review (in which case the existing item will be replaced).

#### Input Parameters
* `id` - _required_ - the id of the review (e.g. "CR-362").

### Adds a review item for each of the supplied crucibleRevisionData elements.

#### Input Parameters
* `id` - _required_ - the id of the review (e.g. "CR-362").

### Removes an item from a review.

#### Input Parameters
* `riId` - _required_ - review item id (e.g. "CFR-6312").
* `id` - _required_ - review id (e.g. "CR-345").

### Returns detailed information for a specific review item.

#### Input Parameters
* `riId` - _required_ - review item id (e.g. "CFR-6312").
* `id` - _required_ - review id (e.g. "CR-345").

### getReviewItemsComments

#### Input Parameters
* `render` - _optional_ - indicate whether to render the wiki text in the returned comments. If set to "true", the comments will contain a
 <messageAsHtml> element containing the wiki rendered html.
* `id` - _required_ - the review perma id

### This call includes the  repsonse header that contains the URL of the newly created entity.

#### Input Parameters
* `riId` - _required_ - the review item id.
* `id` - _required_ - the review perma id

### Sets the review item specified by itemId with the given reviewItem. The old review item is discarded. Can only<br/>
>  perform this operation if the old review item specified by itemId can be deleted. The old review item's permId is<br/>
>  not changed.

#### Input Parameters
* `riId` - _required_ - a valid review item id (e.g. "CFR-5622").
* `id` - _required_ - a valid review id (e.g. "CR-345").

### Removes the revisions given from the review item in the review specified by the id. If the review item has no<br/>
>  more revisions left, it is automatically deleted.

#### Input Parameters
* `rev` - _optional_ - a list of revisions to add to the review item, merging if required. If a revision already exists
 in the given review item, then the given revision is ignored.
* `riId` - _required_ - the id of the review item (e.g. "CFR-5622").
* `id` - _required_ - the id of the review (e.g. "CR-345").

### Adds the given list of revisions to the supplied review item, merging if required. For example, if the review<br/>
>  item for  contains revisions 3 to 6, and if:

#### Input Parameters
* `rev` - _optional_ - a list of revisions to add to the review item, merging if required. If a revision already exists
 in the given review item, then the given revision is ignored.
* `riId` - _required_ - the id of the review item (e.g. "CFR-5622").
* `id` - _required_ - the id of the review (e.g. "CR-345").

### Change the state of a review by performing an action on it.

#### Input Parameters
* `action` - _optional_ - the string representation of the action to perform. Valid actions are:
 
 Note:
* `ignoreWarnings` - _optional_ - if  then condition failure warnings will be ignored

### Get a list of the actions which the current user can perform on this<br/>
>  review, given its current state and the user's permissions.

#### Input Parameters
* `id` - _required_ - the permId of the a review (e.g. "CR-45").

### Uncompletes the review for the current user.

#### Input Parameters
* `ignoreWarnings` - _optional_ - if {@code ignoreWarnings==true} then condition failure warnings will be ignored

### Search for reviews where the name, description, state or permaId contain the specified term.

#### Input Parameters
* `term` - _optional_ - a search term.
* `maxReturn` - _optional_ - the maximum number of reviews to return.

### Get a list of all reviews that have been linked to the specified JIRA issue key.

#### Input Parameters
* `jiraKey` - _optional_ - a Jira issue key (e.g. "FOO-3453")
* `maxReturn` - _optional_ - the maximum number of reviews to return.

### Get a list of all the users. You can also ask for a set of users.

#### Input Parameters
* `username` - _optional_ - a username (or a few) to limit the number of returned entries. It will return only existing users.

### Returns the user details of the user mapped to a committer in a repository.

#### Input Parameters
* `repository` - _required_ - the key of the repository
* `username` - _required_ - the name of the committer

### Returns the user's profile details.

#### Input Parameters
* `username` - _required_ - the username of the user

## License

**flow**ground :- Telekom iPaaS / crucible-local-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
