### My Android Classes ###

Just "Open Sourcing" some of my code I use in my Android development.

##### SimpleAlertDialogFragment Example #####

    AlertDialogFragment dialog = AlertDialogFragment
            .newInstance(android.R.drawable.ic_delete, R.string.alert_title,
                    R.string.pos_text)
            .setOnClickListners(new AlertDialogFragment.AlertDialogOnClickListeners() {
                @Override
                public void doPositiveClick() {
                    Toast.makeText(this, "You did it!", Toast.LENGTH_LONG).show();
                }

                @Override
                public void doNegativeClick() {
                    /* Defaults to closing dialog */
                }
            });
    dialog.show(getSupportFragmentManager(), "delete dialog");
