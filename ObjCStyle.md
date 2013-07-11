# The New Lemurs Guide to Objective-C Style

## General

* Spaces not tabs
* Add whitespace as needed for clarity and explicit grouping.
* Avoid using abbreviations whenever possible
* Consistent use of American English spelling
* Consistent use of whitespace
  * `- (NSString *)stringWithString:(NSString *)string string:(NSString *)string;`
* Newline at end of file
* Eliminated redundant declarations.
* setUp is two words.

## [Headers](./Headers.md)

* Removed redundant import - UIKit and Foundation are already included in the pre-compiled header
* Property qualifier order - Let’s put nonatomic first
* Make properties nonatomic unless they are structs or otherwise noted by comment
* Order properties alphabetically by type
* Group multiple properties of the same type on one line.
* Header order: factories, initializers, properties, actions, additional API

## [Implementation](./Implementation.md)

* Overrides grouped by pragmas named by declaring class and ordered by inheritance hierarchy
* Protocols grouped by named pragmas ordered alphabetically below overrides
* New methods grouped by a pragma named "API" below overrides and protocols
* Implementation declarations terminated by the Oxford semicolon
* Code shape - Use early returns to keep as much code as far left as possible
* Use arc4random_uniform for a properly random number that is not modulo biased
* Order imports alphabetically preceded by the counterpart and followed by frameworks
* Avoid inline constants and label all magic values by declaring explicit constants
* Make use of instancetype return value for all initializers and factories
* Class methods should be above instance methods in their respective sections
* Put early return statements on their own line followed by an empty line.
* User defaults should be registered in +initialize
* Use standardized form for exposing static members.

```ObjC
- (instancetype or type)memberName;
{
    static memberName = nil;
    return memberName ? : (memberName = [[memberName alloc] init]);
}
```
