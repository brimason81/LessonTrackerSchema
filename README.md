# LessonTrackerSchema
This repo outlines the schema for LessonTracker 3.0 

# API Docs

Table of Contents

- [Lessons](#lessons)
- [Lesson Students](#lesson-students)
- [Assignments](#assignments)
- [Student Assignments](#students-assignments)

- [Instruments](#instruments)
- [Student Instruments](#student-instruments)


<a id="lessons"></a>
## Lessons 


```javascript
{
  lessonId: number,
  teacherId: number,
  startTime: Date,
  duration: number, // durationMinutes ( 30 ) ? durationHours ( 0.5 )?
  description: string

  createdAt: Date,
}
```

<a id="lesson-students"></a>
## Lesson Students

```javascript
{
  lessonId: number,
  studentId: number
}
```


<a id="instruments"></a>
## Instruments

```javascript
{
  instrumentId: number,
  name: string    // "guitar", "bass guitar", "piano", etc
}
```


<a id="student-instruments"></a>
## Student Instruments

```javascript
{
  instrumentId: number,
  studentId: number,
  experienceYears: number
}
```
