
* State snapshots fail because the reverted to snapshot may not have future patches from other actors
* Keep track of patches
* On failures
  * Rewind to a known good state
  * Apply all the successful patches after that

    Created at: 2022-09-01
    Updated at: 2022-09-01

