Homework Overview

This Homework simulates a defense session for homework assignments where N students are defended by a professor and an assistant. The professor can handle two defenses simultaneously but will not proceed unless two students are ready. The assistant, however, can handle only one student at a time. Each defense session is modeled using separate threads — one for the assistant and two for the professor. The defenses can commence only when both assistant and professor threads are ready.
Simulation Details

    Duration of Defense Window: The professor and assistant are available for 5 seconds from the start, after which no new defenses can begin.
    Student Arrival: Each student arrives at a random time between 0 and 1 second from the start of the session.
    Defense Duration: Each student takes a random amount of time between 0.5 and 1 second to defend, after which they receive a grade.
    Professor's Requirement: The professor requires two students to start the defense. If only one student is available, the professor will wait.
    Assistant's Operation: The assistant starts the defense as soon as a student is ready.
    Probability: There's a 50% chance for a student to defend with either the professor or the assistant.
    Grading: Each student receives a grade between 5 and 10 upon completion of their defense.

Constraints

    A defense that has started must be completed within 5 seconds; otherwise, it should be interrupted when the time limit expires.
    Each student can only defend once and cannot start a defense after the 5-second window.
    The professor and the assistant cannot assess the same student simultaneously.

Output Format

For each student who either completes their defense or is interrupted, the output should be in the following format:

sql

Thread: <Thread name of the student> Arrival: <Arrival time of the student from the start of the defense> Prof: <Thread name of the assistant or professor> TTC: <Time taken to review the homework>:<Start time of the defense> Score: <Grade received from 5 to 10>

Implementation Notes

    Use a thread pool for creating threads (except singleThreadPool).
    Implement a CyclicBarrier for the professor to handle the scenario where two students are needed for starting the defense.

Objective:

After the 5-second defense window, calculate and print the average score of all students based on the grades received. This average should be accurate regardless of the number of students.
