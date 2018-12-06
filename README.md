Ambient Loop Measures for OpenStudio
====================================

This repository contains several measures needed for creating and running ambient loop-based analyses using 
OpenStudio.


## Testing

To test the measures, you must have the ambient-loop branch checked out of the OpenStudio Standards project. 
To checkout and configure do the following.

1. Install OpenStudio (>= 2.7.1)
1. On OSX, go to /Applications/OpenStudio-2.7.1/Ruby and update the Gemfile to replace the openstudio-standards line with the following:

    ```ruby
    gem 'openstudio-standards', :github => 'NREL/openstudio-standards', :branch => 'ambient-loop'
    ```

1. Run `bundle install --path gems`
1. Go to the `ambient_loop_add_ets_system` directory and run the following to run the tests:

    ```bash
    openstudio --bundle /Applications/OpenStudio-2.7.1/Ruby/Gemfile --bundle_path /Applications/OpenStudio-2.7.1/Ruby/gems measure -r .
    ``` 
 