# Harness delivery acceptance fixture

This branch isolates a GitHub delivery protocol test from the Android app.
A pull request introduces `harness-acceptance/verdict.txt`. CI reports a concrete
file/line error unless its only line is `PASS`. The repair worker should change
only that marker and verify it with `test "$(cat harness-acceptance/verdict.txt)" = PASS`.
No Android application code, default branch, deployment, or release is changed.
