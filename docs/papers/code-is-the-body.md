# Code Is the Body

**Agent-Owned Software Bodies for Recursive Evolution and Descent**<br>
Roy Zhao and Zhenyu Zhao, 2026

[arXiv abstract](https://arxiv.org/abs/2607.28691) ·
[HTML](https://arxiv.org/html/2607.28691v1) ·
[PDF](https://arxiv.org/pdf/2607.28691) ·
[DOI](https://doi.org/10.48550/arXiv.2607.28691)

## What the paper establishes

The paper presents OurArk as an architecture for persistent personal agents
centered on an identity-bearing software body under human custody. It separates
four roles:

- the versioned body containing behavior-defining artifacts and its governed
  change process;
- private instance state such as credentials, memories, logs, and queues;
- a replaceable external reasoner; and
- a human custodian who retains authority over mission, permissions,
  deployment, and promotion.

It defines three body operations: governed evolution of an existing body,
recursive descent into an independently versioned agent with fresh private
state, and selective transfer from a parent or peer after bodies diverge.

## Evaluated public snapshot

The paper is a frozen research record. Later default-branch and release work is
not part of its evaluated implementation snapshot.

| Artifact | Evaluated release | Immutable commit | Reported result |
| --- | --- | --- | --- |
| [Genesis](https://github.com/our-ark/genesis) | [v0.1.1](https://github.com/our-ark/genesis/releases/tag/v0.1.1) | [`e7bb896`](https://github.com/our-ark/genesis/commit/e7bb896411db0d82710fab50c1978b825297844f) | 29/29 tests passed |
| [Enoch](https://github.com/our-ark/enoch) | [v0.3.1](https://github.com/our-ark/enoch/releases/tag/v0.3.1) | [`1021e1d`](https://github.com/our-ark/enoch/commit/1021e1dacce85f4a2edebd865673671bb37a2142) | 753/753 body tests passed |
| Genesis × Enoch | The two releases above | The two commits above | Descendant birth and inherited validation passed |

For current behavior and compatibility, use the
[latest Genesis release](https://github.com/our-ark/genesis/releases/latest)
and [latest Enoch release](https://github.com/our-ark/enoch/releases/latest).

## Evolution-source terminology

The paper counts six origins from which a governed body change can begin:
explicit user requests, feedback, experience, direct-parent inheritance,
cross-agent learning, and brainstorming.

Enoch documentation also refers to four *Evolution candidate pathways*:
feedback, experience, learning, and brainstorming. These counts describe
different boundaries. Direct user requests and selected parent changes enter
the normal task workflow without first becoming Evolution candidates.

```text
explicit user request --------------------> normal task workflow
direct-parent inheritance ----------------> inheritance/task workflow
feedback -----------+
experience ---------+----------------------> Evolution candidate pool
learning -----------+
brainstorming ------+
```

## Reproducing the frozen snapshot

Check out the two evaluated releases in adjacent repository directories. Run
the Genesis suite from the Genesis checkout:

```bash
python -m unittest -q tests/test_genesis_creator.py
```

Install Enoch's locked build prerequisite and run the inherited body suite from
the Enoch checkout:

```bash
python -m pip install --disable-pip-version-check --require-hashes \
  -r .github/requirements/test-build.txt
python -m unittest discover -s tests -t .
```

Then run the cross-artifact descent gate from the Genesis checkout:

```bash
python scripts/verify_enoch_descent.py \
  --source ../enoch \
  --ref HEAD \
  --name my-agent
```

The source checkouts must be clean and remain pinned to Genesis v0.1.1 and
Enoch v0.3.1 for this to reproduce the paper's snapshot rather than current
development.

## Citation

```bibtex
@article{zhao2026code,
  title = {Code Is the Body: Agent-Owned Software Bodies for Recursive Evolution and Descent},
  author = {Zhao, Roy and Zhao, Zhenyu},
  journal = {arXiv preprint arXiv:2607.28691},
  year = {2026},
  doi = {10.48550/arXiv.2607.28691},
  url = {https://arxiv.org/abs/2607.28691}
}
```

Cite the paper for the OurArk architecture. When reporting work performed with
a particular implementation, also cite the exact Genesis or Enoch software
release through that repository's `CITATION.cff`.
