!SLIDE purple

# Suggestions

!SLIDE purple

# Write testable code

!SLIDE

# Structure your JS code
# into functions or objects

!SLIDE

# Isolate components
# From the DOM

!SLIDE

# Isolate AJAX
# to avoid brittle tests

!SLIDE

# Separate into files

!SLIDE purple

# Write good tests

!SLIDE

# Always test methods

!SLIDE

# Mostly test event bindings

!SLIDE

# Write custom matchers

!SLIDE

# Use mocks
## to isolate components

!SLIDE

## You don't own AJAX
# don't mock it

!SLIDE

# Treat templates as fixtures
## Update them manually

!SLIDE

# Write integration tests

!SLIDE code small

# Capybara

    @@@ruby
    visit('/todos')
    fill_in('Description', :with => 'Walk the dog')
    click_button('Create')
    page.should have_selector('.task', :text => 'Walk the dog')

!SLIDE

# Simplify your DOM
# Simplify your templates
