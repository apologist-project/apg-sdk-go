# Reference
## Chat
<details><summary><code>client.Chat.ListChatCompletions() -> *apgsdkgo.ListChatCompletionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a paginated list of chat completions (prompts) for the agent, with applied tags expanded as { id, name } and share metadata.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ListChatCompletionsRequest{}
client.Chat.ListChatCompletions(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Results per page (clamped to 100).
    
</dd>
</dl>

<dl>
<dd>

**agentID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**channelID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**bibleID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**cached:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**client:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**configID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**conversationID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**deviceID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**flagged:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**favorited:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**language:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**liked:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**sessionID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**minTimestamp:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**maxTimestamp:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Chat.CreateChatCompletion(request) -> *apgsdkgo.ChatCompletionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a chat completion using the agent's configured model. Supports both streaming and non-streaming responses.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ChatCompletionRequest{
    Unknown: map[string]any{
        "key": "value",
    },
}
client.Chat.CreateChatCompletion(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*apgsdkgo.ChatCompletionRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Chat.LikeCompletion(ID, request) -> *apgsdkgo.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates the like status of a specific chat completion
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.LikeRequest{
    ID: "id",
    Liked: true,
}
client.Chat.LikeCompletion(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The ID of the chat completion
    
</dd>
</dl>

<dl>
<dd>

**liked:** `bool` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Chat.FlagCompletion(ID, request) -> *apgsdkgo.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates the flagged status of a specific chat completion
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.FlagRequest{
    ID: "id",
    Flagged: true,
}
client.Chat.FlagCompletion(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The ID of the chat completion
    
</dd>
</dl>

<dl>
<dd>

**flagged:** `bool` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Chat.FeedbackCompletion(ID, request) -> *apgsdkgo.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Adds user feedback to a specific chat completion
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.FeedbackRequest{
    ID: "id",
    Feedback: "feedback",
}
client.Chat.FeedbackCompletion(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The ID of the chat completion
    
</dd>
</dl>

<dl>
<dd>

**feedback:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Chat.ShareCompletion(ID, request) -> *apgsdkgo.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a share record for a specific chat completion
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ShareRequest{
    ID: "id",
}
client.Chat.ShareCompletion(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The ID of the chat completion
    
</dd>
</dl>

<dl>
<dd>

**conversationID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**sessionID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Chat.GetChatCompletion(ID) -> *apgsdkgo.GetChatCompletionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a single chat completion (prompt) by numeric id or UUID, including applied tags, guardrail/cta metadata, share metadata, and automation results.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.GetChatCompletionRequest{
    ID: "id",
}
client.Chat.GetChatCompletion(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The numeric id or UUID of the chat completion
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Corpus
<details><summary><code>client.Corpus.SearchCorpus(request) -> *apgsdkgo.SearchCorpusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Performs a semantic search across the agent's corpus of knowledge
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.CorpusSearchRequest{
    Query: "query",
}
client.Corpus.SearchCorpus(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**query:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**promptID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**filters:** `*apgsdkgo.CorpusSearchRequestFilters` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Corpus.LogCorpusView(Model, ID, request) -> *apgsdkgo.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Records that a user viewed a specific corpus item
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ViewRequest{
    Model: "model",
    ID: "id",
    PromptID: "prompt_id",
}
client.Corpus.LogCorpusView(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**model:** `string` — The model type (e.g., 'source')
    
</dd>
</dl>

<dl>
<dd>

**id:** `string` — The ID of the corpus item
    
</dd>
</dl>

<dl>
<dd>

**promptID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Corpus.LogCorpusImpression(Model, ID, request) -> *apgsdkgo.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Records that a corpus item was shown to a user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ImpressionRequest{
    Model: "model",
    ID: "id",
    PromptID: "prompt_id",
}
client.Corpus.LogCorpusImpression(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**model:** `string` — The model type (e.g., 'source')
    
</dd>
</dl>

<dl>
<dd>

**id:** `string` — The ID of the corpus item
    
</dd>
</dl>

<dl>
<dd>

**promptID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Corpus.LogCorpusReferralRedirect(Model, ID) -> *apgsdkgo.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Records a referral for a corpus item and, when a `url` is supplied, issues a 302 redirect to it. Without a `url`, responds with a success message. Requires either the search API entitlement or a same-origin request.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.LogCorpusReferralRedirectRequest{
    Model: "model",
    ID: "id",
    PromptID: "prompt_id",
}
client.Corpus.LogCorpusReferralRedirect(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**model:** `string` — The model type (e.g., 'source')
    
</dd>
</dl>

<dl>
<dd>

**id:** `string` — The numeric ID of the corpus item
    
</dd>
</dl>

<dl>
<dd>

**promptID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**url:** `*string` — URL-encoded destination to redirect to after logging the referral.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Corpus.LogCorpusReferral(Model, ID, request) -> *apgsdkgo.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Records that a user was referred to a corpus item
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ReferralRequest{
    Model: "model",
    ID: "id",
    PromptID: "prompt_id",
}
client.Corpus.LogCorpusReferral(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**model:** `string` — The model type (e.g., 'source')
    
</dd>
</dl>

<dl>
<dd>

**id:** `string` — The ID of the corpus item
    
</dd>
</dl>

<dl>
<dd>

**promptID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**userID:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Evaluators
<details><summary><code>client.Evaluators.ListEvaluations(ID) -> *apgsdkgo.ListEvaluationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a paginated list of evaluations for the evaluator, scoped to the requesting agent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ListEvaluationsRequest{
    ID: "id",
}
client.Evaluators.ListEvaluations(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The ID or key of the evaluator
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Results per page (clamped to 100).
    
</dd>
</dl>

<dl>
<dd>

**minTimestamp:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**maxTimestamp:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**minDuration:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**maxDuration:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**minScore:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**maxScore:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**passed:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**benchmark:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**benchmarkRunID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**benchmarkQuestionID:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Evaluators.EvaluateContent(ID, request) -> *apgsdkgo.EvaluateContentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Runs an evaluation on the provided content using the specified evaluator
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.EvaluatorRequest{
    ID: "id",
    Content: &apgsdkgo.EvaluatorRequestContent{
        String: "content",
    },
}
client.Evaluators.EvaluateContent(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The ID or key of the evaluator
    
</dd>
</dl>

<dl>
<dd>

**frequencyPenalty:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**confidenceThreshold:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**content:** `*apgsdkgo.EvaluatorRequestContent` 
    
</dd>
</dl>

<dl>
<dd>

**model:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**presencePenalty:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**reasoningEffort:** `*apgsdkgo.EvaluatorRequestReasoningEffort` 
    
</dd>
</dl>

<dl>
<dd>

**verbosity:** `*apgsdkgo.EvaluatorRequestVerbosity` 
    
</dd>
</dl>

<dl>
<dd>

**temperature:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**topP:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**variables:** `map[string]*string` — Flat string key/value pairs substituted into `{key}` placeholders in the evaluator prompt. Reserved keys (`options`, `option_descriptions`, `criteria`) cannot be overridden. Not persisted; omitted from the response.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Evaluators.GetEvaluation(ID, EvaluationID) -> *apgsdkgo.GetEvaluationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a single evaluation for the evaluator, scoped to the requesting agent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.GetEvaluationRequest{
    ID: "id",
    EvaluationID: "evaluationId",
}
client.Evaluators.GetEvaluation(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The id or key of the evaluator
    
</dd>
</dl>

<dl>
<dd>

**evaluationID:** `string` — The id or UUID of the evaluation
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## CTAs
<details><summary><code>client.CtAs.MatchCtas(request) -> *apgsdkgo.MatchCtasResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Finds matching CTAs based on conversation context, user, session, device, or messages
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.CtaMatchRequest{
    Unknown: map[string]any{
        "key": "value",
    },
}
client.CtAs.MatchCtas(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*apgsdkgo.CtaMatchRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.CtAs.LogCtaClick(ID, request) -> *apgsdkgo.SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Records that a user clicked on a specific CTA
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.CtaClickRequest{
    ID: "id",
    PromptID: "prompt_id",
}
client.CtAs.LogCtaClick(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The ID of the CTA
    
</dd>
</dl>

<dl>
<dd>

**promptID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Users
<details><summary><code>client.Users.ListUsers() -> *apgsdkgo.ListUsersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a paginated list of users for the agent's team, with applied tags expanded as { id, name } and the persisted responder id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ListUsersRequest{}
client.Users.ListUsers(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Results per page (clamped to 100).
    
</dd>
</dl>

<dl>
<dd>

**externalID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `*string` — Comma-separated tag ids.
    
</dd>
</dl>

<dl>
<dd>

**responderID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**minTimestamp:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**maxTimestamp:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.ListUserFlags() -> *apgsdkgo.ListUserFlagsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a paginated list of user flag definitions for the agent's team (all columns from user_flags), ordered by id ascending.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ListUserFlagsRequest{}
client.Users.ListUserFlags(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Results per page (clamped to 100).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.GetUser(UserID) -> *apgsdkgo.GetUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a single user by external id or internal id, with expanded tags and the persisted responder for the agent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.GetUserRequest{
    UserID: "user_id",
}
client.Users.GetUser(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**userID:** `string` — The user's external id or internal id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Users.UpdateUser(UserID, request) -> *apgsdkgo.UpdateUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates a user's external_id and/or tags and upserts the persisted responder for the agent. Only provided fields are changed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.UserUpdateRequest{
    UserID: "user_id",
}
client.Users.UpdateUser(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**userID:** `string` — The user's external id or internal id
    
</dd>
</dl>

<dl>
<dd>

**externalID:** `*string` — Your external identifier for the user.
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]*apgsdkgo.UserUpdateRequestTagsItem` — Applied tags as a mix of existing tag ids and/or default-language tag names. Unknown ids or names are rejected. Tags are mirror-owned and never created here.
    
</dd>
</dl>

<dl>
<dd>

**responderID:** `*int` — Responder to persist for this user on the requesting agent. Must be active on the agent.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Benchmarks
<details><summary><code>client.Benchmarks.ListBenchmarkRuns(ID) -> *apgsdkgo.ListBenchmarkRunsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a paginated list of runs for a benchmark, scoped to the requesting agent. Each run carries nested evaluators, questions, and a flat evaluations array.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ListBenchmarkRunsRequest{
    ID: "id",
}
client.Benchmarks.ListBenchmarkRuns(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The id or key of the benchmark
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Results per page (clamped to 100).
    
</dd>
</dl>

<dl>
<dd>

**minTimestamp:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**maxTimestamp:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**minDuration:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**maxDuration:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**minScore:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**maxScore:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**passed:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**minResponses:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**maxResponses:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Benchmarks.RunBenchmark(ID, request) -> map[string]any</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Executes a benchmark run and returns the aggregated result with nested evaluators, questions, and a flat evaluations array.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.BenchmarkRunRequest{
    ID: "id",
}
client.Benchmarks.RunBenchmark(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The id or key of the benchmark
    
</dd>
</dl>

<dl>
<dd>

**content:** `*apgsdkgo.BenchmarkRunRequestContent` — Content to evaluate. Required when `source_id` is supplied.
    
</dd>
</dl>

<dl>
<dd>

**completionID:** `*string` — Completion UUID whose stored response should be evaluated.
    
</dd>
</dl>

<dl>
<dd>

**sourceID:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**model:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**numResponses:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**useQuestionVariants:** `*bool` 
    
</dd>
</dl>

<dl>
<dd>

**reasoningEffort:** `*apgsdkgo.BenchmarkRunRequestReasoningEffort` 
    
</dd>
</dl>

<dl>
<dd>

**verbosity:** `*apgsdkgo.BenchmarkRunRequestVerbosity` 
    
</dd>
</dl>

<dl>
<dd>

**scoreThreshold:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**valueThreshold:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**temperature:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**topP:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**frequencyPenalty:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**presencePenalty:** `*float64` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Benchmarks.GetBenchmarkRun(ID, RunID) -> *apgsdkgo.GetBenchmarkRunResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a single benchmark run by id or UUID, scoped to the requesting agent, including nested evaluators, questions, and evaluations.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.GetBenchmarkRunRequest{
    ID: "id",
    RunID: "runId",
}
client.Benchmarks.GetBenchmarkRun(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The id or key of the benchmark
    
</dd>
</dl>

<dl>
<dd>

**runID:** `string` — The id or UUID of the run
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Channels
<details><summary><code>client.Channels.GetDiscordChannelStatus(ID) -> *apgsdkgo.GetDiscordChannelStatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the status of the Discord channel. Used as a lightweight health/verification endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.GetDiscordChannelStatusRequest{
    ID: "id",
}
client.Channels.GetDiscordChannelStatus(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The channel id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Channels.ReceiveDiscordInteraction(ID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Receives Discord interaction callbacks for the channel. Requests are verified via Ed25519 signature headers; unsigned or invalid requests are rejected. Payload shape is defined by Discord.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ReceiveDiscordInteractionRequest{
    ID: "id",
    SignatureEd25519: "x-signature-ed25519",
    SignatureTimestamp: "x-signature-timestamp",
    Body: map[string]any{
        "key": "value",
    },
}
client.Channels.ReceiveDiscordInteraction(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The channel id
    
</dd>
</dl>

<dl>
<dd>

**signatureEd25519:** `string` — Discord request signature (hex).
    
</dd>
</dl>

<dl>
<dd>

**signatureTimestamp:** `string` — Discord request timestamp.
    
</dd>
</dl>

<dl>
<dd>

**request:** `map[string]any` — Discord interaction payload.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Channels.VerifyFacebookWebhook(ID) -> string</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the Meta webhook verification handshake, echoing `hub.challenge` when `hub.verify_token` matches the channel's configured token.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.VerifyFacebookWebhookRequest{
    ID: "id",
    HubMode: apgsdkgo.VerifyFacebookWebhookRequestHubModeSubscribe,
    HubVerifyToken: "hub.verify_token",
}
client.Channels.VerifyFacebookWebhook(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The channel id
    
</dd>
</dl>

<dl>
<dd>

**hubMode:** `*apgsdkgo.VerifyFacebookWebhookRequestHubMode` 
    
</dd>
</dl>

<dl>
<dd>

**hubVerifyToken:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**hubChallenge:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Channels.ReceiveFacebookMessage(ID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Receives Facebook/Messenger (and Instagram-style) message events for the channel. Payload shape is defined by Meta.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ReceiveFacebookMessageRequest{
    ID: "id",
    Body: map[string]any{
        "key": "value",
    },
}
client.Channels.ReceiveFacebookMessage(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The channel id
    
</dd>
</dl>

<dl>
<dd>

**request:** `map[string]any` — Meta webhook payload.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Channels.GetInstagramPrivacyPolicy(ID) -> string</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a static HTML privacy policy page for the Instagram integration.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.GetInstagramPrivacyPolicyRequest{
    ID: "id",
}
client.Channels.GetInstagramPrivacyPolicy(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The channel id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Channels.ReceiveTelegramUpdate(ID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Receives Telegram bot update events for the channel. Non-message updates are acknowledged and ignored. Payload shape is defined by Telegram.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ReceiveTelegramUpdateRequest{
    ID: "id",
    Body: map[string]any{
        "key": "value",
    },
}
client.Channels.ReceiveTelegramUpdate(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The channel id
    
</dd>
</dl>

<dl>
<dd>

**request:** `map[string]any` — Telegram update payload.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Channels.ReceiveTwilioMessage(ID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Receives inbound Twilio messages for the channel as form-encoded data. Payload fields are defined by Twilio.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.ReceiveTwilioMessageRequest{
    ID: "id",
}
client.Channels.ReceiveTwilioMessage(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The channel id
    
</dd>
</dl>

<dl>
<dd>

**from:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**body:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Shares
<details><summary><code>client.Shares.GetSharedMessages(Token) -> *apgsdkgo.GetSharedMessagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Public, unauthenticated read of the messages behind a share token. The token is the bearer capability and enforces tenant isolation against the host agent. An empty or invalid token yields an empty messages array.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &apgsdkgo.GetSharedMessagesRequest{
    Token: "token",
}
client.Shares.GetSharedMessages(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**token:** `string` — The share token
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

