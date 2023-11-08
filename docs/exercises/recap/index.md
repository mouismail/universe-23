# :test_tube: Review of Workshop Outcomes

So far, we have reached the following milestones, learning to

- [x] Track work on GitHub
- [x] Rapidly onboard onto an existing project
- [x] Work in a collaborative manner, and enable quick incorporation of feedbacks
- [x] Efficiently secure the software supply chain, catching vulnerabilities and non-compliant dependencies as they are introduced
- [x] Automate versioning
- [x] Automate releases
- [x] Implement continuous deployment

## Process Summary

```mermaid
flowchart TD
    subgraph Checks
        A[Code Scanning]
        B[Build]
        C[Functional Test]
        D[Workflow Failure]
    end

    A-->|Pass|B
    A-->|Fail|D
    B-->|Pass|C
    B-->|Fail|D
    C-->|Pass|K
    C-->|Fail|D

    subgraph Release Process
        E[Version]
        F[Create Release Asset]
        G[Draft Release]
        H[Upload Asset to Draft Release]
        I[Publish Release]
        J[Failure Workflow]

    end

    E-->|Success|F
    F-->|Success|G
    F-->|Fail|J
    G-->|Valid|H
    G-->|Invalid|J
    H-->|Pass|I
    H-->|Fail|J
    E-->|Fail|J

    subgraph Main Branch
        K[Push to Main Branch]
    end

    K-->|Success|E

```

## Observations

Let us observe the outcome of the exercises we have completed as a whole.

1. Navigate to the `Actions` tab and verify the workflows are running (or have completed running).
2. Check the tag was created on the repository.
3. Check the release was created on the repository.
4. Check the release was created on the repository.
