# Software incident export

An original **synthetic teaching dataset** created for this course. It contains
no customer records or observations from a real company.

Use the same `software_incidents.csv` in Sessions 1 and 2. Its 25 exported rows
describe 24 fictional closed incidents and one repeated export record. The
intended observational unit is one incident. An export row is not necessarily
a distinct incident. Blank durations represent unknown logged resolution times,
not incidents still open. A negative duration is a logging error. One service
label is missing. Preserve the raw file while investigating these issues.

The fictional target population is all closed incidents in these services
during the imagined reporting period. The export has no probability sampling
design. Versions were not randomly assigned; do not infer a causal deployment
effect or generalize to real systems. Service and severity are deliberately
associated, so this example cannot separate their effects.

See `data_dictionary.md` for units and valid values. The original dataset assets
are offered under CC0 1.0; see `LICENSE.txt`. External readings retain their own
licences.

Download the CSV and upload it with the notebook in Colab, or use the embedded
identical copy in each notebook to work offline. No external data URL is needed.
Later sessions must reconsider suitability for their inferential goals.
