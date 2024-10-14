# Change default shell to fish

1. memo fish path

   ```shell
   which fish
   ```

1. add fish to shells

   ```shell
   sudo -e /etc/shells
   ```

1. open PreferencePanes > Users & Groups Pane

   ```
   open -b com.apple.systempreferences /System/Library/PreferencePanes/Accounts.prefPane
   ```

1. Ctrl+click user

   ![01_users_and_groups_pane](uploads/change_default_shell_to_fish/01_users_and_groups_pane.png)

1. choose shell

   ![02_users_and_groups_pane](uploads/change_default_shell_to_fish/02_users_and_groups_pane.png)
