# Intended Use

**What it is.** Iasis is a research tool that predicts whether a small
molecule is likely to cross the blood-brain barrier (BBB), and suggests
structural modifications that may improve permeability. Predictions come
with calibrated uncertainty and an explicit applicability domain.

**Who it is for.** Researchers and students in medicinal chemistry,
pharmacology and neuroscience, triaging candidate molecules in early
discovery or learning the methods.

**What it is not.**
- Not a medical device. It gives no diagnosis, treatment or dosing advice.
- Not a drug discovery system. It generates and ranks hypotheses; it does
  not identify drug candidates.
- Not a replacement for experiment. Every prediction is a prior to be
  tested in vitro.
- Not validated for antibodies, biologics, or any molecule outside its
  stated applicability domain.

**Data in.** Public sources only: Therapeutics Data Commons, ChEMBL,
PubChem, PubMed, openFDA. No patient data, no personal data, no
proprietary datasets.

**Data out — zero retention.** Structures submitted by users are never
stored. Logs record a timestamp, runtime, and whether the request was
refused. No SMILES, no structures, no molecular identifiers are
persisted anywhere. Usage is measured only in aggregate statistics that
cannot reconstruct an input.

**Refusal is a feature.** When a query falls outside the model's
applicability domain, Iasis returns no permeability prediction. It
returns instead the computed descriptors, the similarity to the nearest
training examples, and the reason for refusal. A fabricated number is
worse than no number.

**Human in the loop.** Iasis ranks and explains. A chemist decides what
to synthesise and a laboratory decides what is true. No output of this
system is an authorisation to act.

**Limitations.** Documented per release in `MODEL_CARD.md`: performance
by chemical class, calibration curves, and the applicability-domain
threshold with the measurement that set it.
