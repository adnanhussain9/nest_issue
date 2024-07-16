# nest_issue
issues encountered and solution

**1. Pre-save for schema**
solution: 

https://github.com/nestjs/mongoose/issues/264

UserSearchSchema.pre<UserSearch>('save', function (next: Function) {
    if (!this.isNew) {
        this.updatedAt = new Date();
    }
    next();
});
