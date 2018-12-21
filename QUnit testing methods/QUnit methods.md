# QUnit Testing Methods

* [__Module__](#user-content-module)
* [__Only__](#user-content-only)
* [__Skip__](#user-content-skip)
* [__Todo__](#user-content-todo)

___

### Module

You can use the module name to organize, select, and filter tests to run. All tests inside a module callback function will be grouped into
that module. The test names will all be preceded by the module name in the test results.

        let { module,test } = QUnit
        module( "group a" );
        test( "a basic test example", function( assert ) {
        assert.ok( true, "this test is fine" );
        });
        
        test( "a basic test example 2", function( assert ) {
          assert.ok( true, "this test is fine" );
        });
 
 ### Only
Use this method to focus your test suite on a specific test. QUnit.only will cause any other tests in your suite to be ignored.
If more than one QUnit.only is present only the first instance will run.
        
        let { module,test } = QUnit
        module( "robot", {
          beforeEach: function() {
            this.robot = new Robot();
          }
        });

        test( "say", function( assert ) {
          assert.ok( false, "I'm not quite ready yet" );
        });
        only( "laser", function( assert ) {
          assert.ok( this.robot.laser() );
        });
        
### Skip

This test’s prototype will be listed on the suite as a skipped test, ignoring the callback argument and the respective globas 
and module’s hooks.
        
        let { module,test } = QUnit
        module( "robot", {
          beforeEach: function() {
            this.robot = new Robot();
          }
        });
        
        test( "say", function( assert ) {
          assert.strictEqual( this.robot.say(), "Exterminate!" );
        });
        skip( "laser", function( assert ) {
          assert.ok( this.robot.laser() );
        });
        
### Todo

This method is used to test a unit of code which is still under development (in a “todo” state). The test will pass as long as one failing assertion is present.  

        QUnit.module( "robot", {
          beforeEach: function() {
            this.robot = new Robot();
          }
        });

        QUnit.todo( "fireLazer returns the correct value", function( assert ) {
          var result = this.robot.fireLazer(); 
          assert.equal( result, "I'm firing my lazer!" );
        });